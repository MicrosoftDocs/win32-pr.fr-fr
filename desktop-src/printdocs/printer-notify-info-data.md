---
description: La \_ structure de \_ \_ données d’informations de notification d’imprimante identifie un champ de travail ou d’informations sur l’imprimante et fournit les données actuelles pour ce champ.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Structure PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203282"
---
# <a name="printer_notify_info_data-structure"></a>\_Structure de \_ données d’informations de notification d’imprimante \_

La structure de **\_ \_ \_ données** d’informations de notification d’imprimante identifie un champ de travail ou d’informations sur l’imprimante et fournit les données actuelles pour ce champ.

La fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retourne une structure d' [**\_ \_ informations de notification d’imprimante**](printer-notify-info.md) , qui contient un tableau de structures de **\_ \_ \_ données d’informations de notification d’imprimante** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Indique le type d’informations fournies. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                      | Signification                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Travail \_ \_Type de notification**</dt> <dt>0x01</dt> </dl>             | Indique que le membre **champ** spécifie une \_ constante de champ de notification de travail \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Imprimante \_ \_Type de notification**</dt> <dt>0x00</dt> </dl> | Indique que le membre **champ** spécifie une \_ constante de champ de notification d’imprimante \_ \_ \* .<br/> |



 

</dd> <dt>

**Champ**
</dt> <dd>

Indique le champ qui a été modifié. Pour obtenir la liste des valeurs possibles, consultez la section Notes.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**Id**
</dt> <dd>

Indique l’identificateur du travail si le membre du **type** spécifie le type de notification du travail \_ \_ . Si le membre de **type** spécifie le \_ type de notification d’imprimante \_ , ce membre n’est pas défini.

</dd> <dt>

**NotifyData**
</dt> <dd>

Union d’informations de données basées sur les membres du **type** et du **champ** . Pour obtenir une description du type de données associé à chaque champ, consultez la section Notes.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Tableau de deux valeurs **DWORD** . Pour les champs d’informations qui n’utilisent qu’une seule **valeur DWORD**, les données se trouvent dans **adwData** \[ 0 \] .

</dd> <dt>

**Données**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indique la taille, en octets, de la mémoire tampon vers laquelle pointe **pBuf**.

</dd> <dt>

**pBuf**
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les données actuelles du champ.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Si le membre de **type** spécifie le \_ type de notification d’imprimante \_ , le membre de **champ** peut prendre l’une des valeurs suivantes.



<table>
<thead>
<tr class="header">
<th>Champ</th>
<th>Type de données</th>
<th>Valeur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>Non pris en charge.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’imprimante.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui identifie le point de partage de l’imprimante.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom du port sur lequel les travaux d’impression seront imprimés. Si &quot; &quot; le regroupement d’imprimantes est sélectionné, il s’agit d’une liste de ports séparés par des virgules.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom du pilote de l’imprimante.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient la nouvelle chaîne de commentaire, qui est généralement une brève description de l’imprimante.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nouvel emplacement physique de l’imprimante (par exemple, &quot; Bldg. 38, salle 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf</strong> est un pointeur vers une structure <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> qui définit les données d’imprimante par défaut telles que l’orientation du papier et la résolution.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier utilisé pour créer la page de séparation. Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression utilisé par l’imprimante.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression par défaut.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> est un pointeur vers une structure <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> pour l’imprimante. Le pointeur peut être <strong>null</strong> s’il n’existe aucun descripteur de sécurité.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] spécifie les attributs d’imprimante, qui peuvent être l’une des valeurs suivantes :<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] spécifie une valeur de priorité que le spouleur utilise pour router les travaux d’impression.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] spécifie la valeur de priorité par défaut affectée à chaque travail d’impression.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] spécifie l’heure la plus ancienne à laquelle l’imprimante imprime un travail. (Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] spécifie l’heure la plus récente à laquelle l’imprimante imprime un travail. (Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] spécifie l’état de l’imprimante. Pour obtenir la liste des valeurs possibles, consultez la structure <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Non pris en charge.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] spécifie le nombre de travaux d’impression qui ont été mis en file d’attente pour l’imprimante.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] spécifie le nombre moyen de pages par minute qui ont été imprimées sur l’imprimante.</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>Non pris en charge.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>Non pris en charge.</td>
<td>0x17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>Non pris en charge.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>Non pris en charge.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Cette valeur est définie si le GUID de l’objet change.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Cette valeur est définie si la connexion à l’imprimante est renommée.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Si le membre de **type** spécifie le \_ type de notification de travail \_ , le membre de **champ** peut être l’une des valeurs suivantes.



| Champ                                    | Type de données                                                                                                                                                                                                                                            | Valeur |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| nom de l’imprimante du champ de \_ notification du travail \_ \_ \_        | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’imprimante pour laquelle la tâche est mise en attente.                                                                                                                                      | 0x00  |
| \_nom d' \_ ordinateur du champ de notification du travail \_ \_        | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’ordinateur qui a créé le travail d’impression.                                                                                                                                    | 0x01  |
| \_nom du \_ port du champ de notification du travail \_ \_           | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante. Si une imprimante est connectée à plusieurs ports, les noms des ports sont séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »). | 0x02  |
| \_nom d' \_ utilisateur du champ de notification du travail \_ \_           | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui a envoyé le travail d’impression.                                                                                                                                           | 0x03  |
| \_nom du \_ champ \_ NOTIFIer le travail \_         | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui doit être averti lorsque le travail a été imprimé ou lorsqu’une erreur se produit lors de l’impression du travail.                                                              | 0x04  |
| \_type de \_ données du champ de notification du travail \_             | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.                                                                                                                                         | 0x05  |
| \_processeur d' \_ impression du champ de notification du travail \_ \_     | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression à utiliser pour imprimer le travail.                                                                                                                           | 0x06  |
| \_paramètres du \_ champ de notification du travail \_           | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression.                                                                                                                                                            | 0x07  |
| \_nom du \_ pilote du champ de notification du travail \_ \_         | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante qui doit être utilisé pour traiter le travail d’impression.                                                                                                           | 0x08  |
| champ de notification de tâche \_ \_ \_ DEVMODE              | **pBuf** est un pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient des données d’initialisation d’appareil et d’environnement pour le pilote d’imprimante.                                                                                                        | 0x09  |
| \_État du \_ champ de notification du travail \_               | **adwData** \[ 0 \] spécifie l’état du travail. Pour obtenir la liste des valeurs possibles, consultez la structure [**Job \_ info \_ 2**](job-info-2.md) .                                                                                                                        | 0x0A  |
| \_chaîne d' \_ État du champ de notification du travail \_ \_       | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression.                                                                                                                                                           | 0x0B  |
| \_descripteur de sécurité de champ de notification de travail \_ \_ \_ | Non pris en charge.                                                                                                                                                                                                                                          | 0x0C  |
| \_document de \_ champ de notification de tâche \_             | **pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du travail d’impression (par exemple, « MS-WORD : Review.doc »).                                                                                                                        | 0x0D  |
| \_priorité du \_ champ de notification du travail \_             | **adwData** \[ 0 \] spécifie la priorité du travail.                                                                                                                                                                                                           | 0x0E  |
| \_position du \_ champ de notification du travail \_             | **adwData** \[ 0 \] spécifie la position du travail dans la file d’attente à l’impression.                                                                                                                                                                                      | 0x0F  |
| champ de notification de travail \_ \_ \_ envoyé            | **pBuf** est un pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle le travail a été soumis.                                                                                                                          | 0x10  |
| \_heure de \_ début du champ de notification du travail \_ \_          | **adwData** \[ 0 \] spécifie l’heure à laquelle le travail peut être imprimé au plus tôt. (Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)                                                                                                                | 0x11  |
| champ de notification du travail \_ \_ \_ jusqu’à l' \_ heure          | **adwData** \[ 0 \] spécifie l’heure à laquelle le travail peut être imprimé au plus tard. (Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)                                                                                                                  | 0x12  |
| \_heure du \_ champ de notification du travail \_                 | **adwData** \[ 0 \] spécifie la durée totale, en secondes, qui s’est écoulée depuis le début de l’impression du travail.                                                                                                                                                  | 0x13  |
| \_ \_ \_ nombre total de \_ pages du champ notifier le travail         | **adwData** \[ 0 \] spécifie la taille, en pages, du travail.                                                                                                                                                                                             | 0x14  |
| PAGES de champs de notification de travail \_ \_ \_ \_ imprimées       | **adwData** \[ 0 \] spécifie le nombre de pages qui ont été imprimées.                                                                                                                                                                                      | 0x15  |
| champ de notification du travail- \_ \_ \_ nombre total d' \_ octets         | **adwData** \[ 0 \] spécifie la taille, en octets, du travail.                                                                                                                                                                                             | 0x16  |
| octets du champ de notification du travail \_ \_ \_ \_ imprimés       | **adwData** \[ 0 \] spécifie le nombre d’octets qui ont été imprimés sur ce travail. Pour ce champ, l’objet de notification de modification est signalé lorsque des octets sont envoyés à l’imprimante.                                                                      | 0x17  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_Informations sur le travail \_ 2**](job-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_informations de notification de l’imprimante \_**](printer-notify-info.md)
</dt> <dt>

[**descripteur de sécurité \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

