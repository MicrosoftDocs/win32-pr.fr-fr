---
title: Interface IMsRdpClientAdvancedSettings5
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512574"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>Interface IMsRdpClientAdvancedSettings5

Gère les paramètres client avancés. Dérive de l’interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .

Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings5** à **QueryInterface**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientAdvancedSettings5** hérite de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md). **IMsRdpClientAdvancedSettings5** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientAdvancedSettings5** possède les propriétés suivantes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Mode de redirection audio. La propriété <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> a les valeurs possibles suivantes.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (la redirection audio est activée et l’option de redirection est &quot; Envoyer à cet ordinateur &quot; . Il s’agit du mode par défaut.)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (la redirection audio est activée et l’option &quot; laisse sur l’ordinateur distant &quot; . L' &quot; option de départ sur l’ordinateur distant &quot; est prise en charge uniquement lors de la connexion à distance à un ordinateur hôte qui exécute Windows Vista. Si la connexion est vers un ordinateur hôte qui exécute Windows Server 2008, l’option &quot; conserver sur l’ordinateur distant &quot; est remplacée par &quot; ne pas lire &quot; .)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (la redirection audio est activée et le mode n’est &quot; pas lu &quot; .)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie la taille du fichier de cache virtuel pour les bitmaps de 32 bits par pixel (BPP). La valeur maximale est de 48 mégaoctets (Mo).<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le bouton épingler doit être affiché dans la barre de connexion. Par défaut, la valeur est <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le mode public doit être activé ou désactivé. Par défaut, le mode public a la valeur <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la redirection du presse-papiers doit être activée ou désactivée. Par défaut, le mode de redirection du presse-papiers a la valeur <strong>true</strong> (activé).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si les appareils redirigés doivent être activés ou désactivés. Par défaut, le mode appareils Redirigé est défini sur <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si les appareils redirigés de point de service doivent être activés ou désactivés. Par défaut, le mode appareils redirigés point de service est défini sur <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

