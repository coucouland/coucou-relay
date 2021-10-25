# coucou-relay
An email relay service with smart routing for iCalendar resources

## Overview

The proliferation of iCalendar for more use-cases could lead to an increase in traffic when using email as the messaging transport. Ideally we should be able to intelligently route and filter iCalendar messages that don't require any human intervention.

For example, when new events, notes and tasked are published (from known sources) we can automatically process such messages and keep our Inbox free from clutter. The coucou-relay service can act as an Email relay that can route such messages to different targets based on intelligent routing rules.

## Features

The following features are supported by this email relay service.

### Single-address, multiple destinations

As with most email relay services you can route messages to your Inbox from multiple relay addresses. In addition you can also route to other destinations based on specified rules. e.g.

- Relay address: fou@cloud.coucou.land
- Default destination: fou@example.com
- Rule 1:
    - Destination type: email
    - Destination address: notes@example.com
    - Destination rule: method=publish;component=vtodo

