---
description: Les constantes suivantes constituent l’ensemble des commandes d’appareil matériel WIA (Windows Image Acquisition) valides.
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Commandes de l’appareil WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862666"
---
# <a name="wia-device-commands"></a>Commandes de l’appareil WIA

Les constantes suivantes constituent l’ensemble des commandes d’appareil matériel WIA (Windows Image Acquisition) valides.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Fait en sorte que le minipilote de l’appareil synchronise les éléments mis en cache avec le périphérique matériel. Si l’appareil prend en charge la méthode <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem :: AnalyzeItem</strong></a> , l’émission de cette commande amène le minipilote à abandonner les résultats de l’analyse et à rétablir l’état initial de l’élément. Tous les pilotes doivent prendre en charge cette commande.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Provoque l’acquisition d’une image par un appareil WIA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Indique à l’appareil de supprimer tous les éléments qui peuvent être supprimés de l’arborescence des objets <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> qui représentent l’appareil. La suppression d’éléments est empêchée en définissant les propriétés de l’élément. Pour plus d’informations, consultez <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage :: SetPropertyStream</strong></a> et <a href="-wia-property-attributes.md">attributs de propriété</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Utilisé pour les scanneurs de documents. Fait en sorte que le scanneur charge la page suivante dans son gestionnaire de documents.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Utilisé pour les scanneurs de documents. Indique à l’appareil de décharger toutes les pages restantes dans son gestionnaire de documents. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Utilisé pour les scanneurs de documents qui ont un flux de page. Indique à l’appareil de démarrer le moteur du chargeur. Cette fonctionnalité est disponible à partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Utilisé pour les scanneurs de documents qui ont un flux de page. Indique à l’appareil d’arrêter le moteur du chargeur. Cette fonctionnalité est disponible à partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <strong>WIA_IPS_FEEDER_CONTROL</strong> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Utilisé pour les scanneurs de documents qui ont un flux de page. Indique à l’appareil d’interrompre le moteur du chargeur. Cette fonctionnalité est disponible à partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <strong>WIA_IPS_FEEDER_CONTROL</strong> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
