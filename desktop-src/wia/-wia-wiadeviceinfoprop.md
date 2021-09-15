---
description: 'Constantes de propriété d’informations sur l’appareil : les propriétés des informations de périphérique sont des propriétés qui décrivent la configuration et l’installation de l’appareil.'
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propriété d’informations sur l’appareil (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 29db0a527146218e19b3fe583fd48936f71dac29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521204"
---
# <a name="device-information-property-constants"></a>Constantes de propriété d’informations sur l’appareil

Les propriétés d’informations de périphérique sont des propriétés qui décrivent l’installation et l’installation de l’appareil. Ces propriétés sont disponibles par le biais des interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , ainsi que par le biais de l’élément racine. les propriétés d’informations sur l’appareil sont précédées de « wia \_ DIP \_ » (propriété d’informations de périphérique) et sont fournies par Windows acquisition d’images (wia). À des fins de script, ces constantes utilisent le préfixe « DeviceInfo » et font partie du type énuméré [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante/valeur</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td >Chaîne d’ID de l’appareil pour le minipilote WIA. Le service WIA crée et gère cette propriété.<br/> Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td >Chaîne de description du fournisseur pour le minipilote WIA. La description du fournisseur est obtenue à partir du fichier INF. Une application lit cette propriété pour obtenir une description du fournisseur de l’appareil. Le service WIA crée et gère cette propriété.<br/> Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td >Chaîne de description de l’appareil pour le minipilote WIA. Le service WIA crée et gère cette propriété. La chaîne de description de l’appareil que cette propriété contient est obtenue à partir du fichier INF. Une application lit cette propriété pour obtenir une description de l’appareil.<br/> Type : VT_BSTR, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td >Type d’appareil et sous-type d’appareil. Le service WIA crée et gère cette propriété. Utilisez la macro GET_STIDEVICE_TYPE pour récupérer le type d’appareil. Le type et le sous-type d’appareil sont obtenus à partir du fichier INF. Une application lit cette propriété pour déterminer si elle utilise un scanneur, un appareil photo ou un périphérique vidéo.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Actuellement, les types d’appareils sont définis comme suit. l’astérisque * indique que le type d’appareil n’est pas pris en charge par Windows Vista et versions ultérieures. le double astérisque * * indique que le type d’appareil n’est pas pris en charge par Windows Server 2003, Windows Vista ou version ultérieure. <br/> 
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>StiDeviceTypeDefault</td>
<td>0x0000</td>
<td>Appareil par défaut</td>
</tr>
<tr class="even">
<td>StiDeviceTypeScanner</td>
<td>0x0001</td>
<td>Périphérique scanneur (voir le <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> pour déterminer si le scanneur est à plat ou feuille.)</td>
</tr>
<tr class="odd">
<td>StiDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>Appareil photo</td>
</tr>
<tr class="even">
<td>StiDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>Périphérique vidéo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td ><p>Nom du port de l’appareil installé, affecté par le pilote en mode noyau qui exécute l’appareil. Le service WIA crée et gère cette propriété. Une application lit cette propriété pour déterminer le nom du port.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td ><p>Nom de l’appareil Le service WIA crée et gère cette propriété. Le nom de l’appareil contenu dans cette propriété est obtenu à partir du fichier INF. Une application lit cette propriété pour obtenir le nom de l’appareil.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td ><p>Nom du serveur sur lequel s’exécute le minipilote WIA. cette propriété est facultative pour Windows XP et versions ultérieures.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td ><p>L’ID d’appareil de l’appareil WIA qui est installé sur un ordinateur distant. Le service WIA crée et gère cette propriété. Elle est utilisée uniquement en interne par le service WIA.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td ><p>CLSID fourni par le fournisseur pour tout objet COM d’extension d’interface utilisateur installé avec le minipilote WIA. Le service WIA crée et gère cette propriété. La valeur du CLSID de l’interface utilisateur contenue dans cette propriété est obtenue à partir du fichier INF. Si aucun CLSID d’interface utilisateur n’est spécifié, le service WIA fournit une valeur par défaut. Cette propriété est utilisée uniquement en interne par le service WIA lorsque l’interface utilisateur est affichée.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td ><p>Type de connexion utilisé par l’appareil. Le service WIA crée et gère cette propriété, et seul le service WIA peut la modifier.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La propriété peut avoir les valeurs possibles suivantes.</p>

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Périphérique WDM générique</td>
</tr>
<tr class="even">
<td>2</td>
<td>Périphérique SCSI</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Périphérique USB</td>
</tr>
<tr class="even">
<td>8</td>
<td>Appareil série</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Appareil parallèle</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td ><p>Paramètre de vitesse en bauds actuel de l’appareil. Le service WIA crée et gère cette propriété. La valeur doit être &quot; vide &quot; si l’appareil n’est pas connecté par un câble série.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td ><p>Les fonctionnalités STI génériques pour l’appareil obtenues à partir du fichier INF. Le service WIA crée et gère cette propriété. Une application lit cette propriété pour déterminer les fonctionnalités de STI génériques de l’appareil.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td ><p>Nombre (sous forme de chaîne) de la version WIA actuelle qui est installée sur le système. Une application lit cette propriété pour déterminer la version de WIA qui est installée sur le système. Le service WIA crée et gère cette propriété. cette propriété est disponible dans Windows XP et versions ultérieures.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td ><p>Version actuelle de la DLL du minipilote WIA. Le service WIA crée et gère cette propriété. cette propriété est disponible dans Windows XP et versions ultérieures.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td ><p>ID PnP actuel de l’appareil. Le service WIA crée et gère cette propriété. cette propriété est disponible dans Windows Vista et versions ultérieures.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td ><p>Version du pilote STI générique. Le service WIA crée et gère cette propriété. Une application lit cette propriété pour déterminer la version du pilote STI générique. cette propriété est disponible dans Windows Vista et versions ultérieures.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




