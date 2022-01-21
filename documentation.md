**/api/web-login/token – POST**

| **grant\_type** | password |
| --- | --- |
| **client\_id** | Emos |
| **client\_secret** | 56951025 |
| **username** | admin |
| **Password** | {password} |

**RETURN – JSON**

| **access\_token** | \&lt;token\&gt; string |
| --- | --- |
| **expires\_id** | \&lt;expire-time\&gt; int |
| **token\_type** | Bearer |

When requesting api send Authorization Header with Bearer Token requested here:

![](RackMultipart20220121-4-y458k2_html_88249fa5497a0c08.png)

---

Get smart meter config as protobuf

**/api/data-transfer/protobuf/gdr/local/config/smart-meter – GET**

**RETURN – PROTOBUF**

| **Not yet researched** | unknown |
| --- | --- |

---

Get smart meter system details

**/api/device-settings/devicestatus – GET**

**RETURN – JSON**

| **CpuLoad** | Int |
| --- | --- |
| **CpuTemp** | Int |
| **FlashAppFree** | long |
| **FlashAppTotal** | long |
| **FlashDataFree** | long |
| **FlashDataTotal** | long |
| **RamFree** | Int |
| **RamTotal** | Int |
| **Status** | String \&lt;e.g. idle\&gt; |

---

Get smart meter system real-time-stats

**ws:// \&lt;host\&gt; /api/data-transfer/ws/protobuf/gdr/local/values/smart-meter – WEBSOCKET**

**Socket messages are binary PROTOBUF!**

| **Structure not yet researched** | **todo** |
| --- | --- |

---

Get smart meter tarif data

**/api/tariffs/contract – GET**

**RETURN JSON**

| **version** | **1 int** |
| --- | --- |
| **currency** | **\&lt;currency\&gt; Shorthand string** |
| **days** | **Json obj**

| **Key** | **Value** |
| --- | --- |
| **\&lt;uuid\&gt;** | „**hours&quot; array (24 length)** |

 |
| **monthly\_base\_fee** | **Int** |
| **tariffs** | **JSON obj**

| **Key** | **Value** |
| --- | --- |
| **\&lt;uuid\&gt;** |

| **label** | **String** |
| --- | --- |
| **obis** | **String** |
| **source** | **String** |
| **weekdays** | **Array (uuids)** |

 |

 |
 
 ---

Get smart meter tarif detail data (further research needed)

**/api/tariffs/data/\&lt;uuid\&gt;/1642719600/1642805999 – GET**

**\&lt;time\_from\&gt;/\&lt;time\_to\&gt;**

**RETURN JSON ARRAY**

| **time** | **Int** |
| --- | --- |
| **diff** | **Int** |
| **price** | **int** |

---

Get smart meter modbus infos

**/api/modbus/\&lt;config/presets/groups/sensors\&gt; – GET**

**RETURN JSON**

FURTHER RESEARCH NEEDED

---

Get smart meter system info

**/api/device-settings – GET**

**RETURN JSON**

FURTHER RESEARCH NEEDED

---

Get smart meter network info

**/api/device-settings/network – GET**

**RETURN JSON**

FURTHER RESEARCH NEEDED****
