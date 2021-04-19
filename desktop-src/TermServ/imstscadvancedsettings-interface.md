---
title: Interface IMsTscAdvancedSettings
description: Comprend des méthodes pour récupérer et définir des propriétés qui activent la mise en cache, la compression et la redirection de l’imprimante et du presse-papiers.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, Description
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511149"
---
# <a name="imstscadvancedsettings-interface"></a>Interface IMsTscAdvancedSettings

Comprend des méthodes pour récupérer et définir des propriétés qui activent la mise en cache, la compression et la redirection de l’imprimante et du presse-papiers. Vous pouvez également spécifier les noms des dll clientes du canal virtuel.

Vous obtenez une instance de cette interface à l’aide de la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) .

## <a name="members"></a>Membres

L’interface **IMsTscAdvancedSettings** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscAdvancedSettings** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsTscAdvancedSettings** possède les propriétés suivantes.



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
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le mode d’entrée d’arrière-plan est activé.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la mise en cache bitmap est activée.<br/>
<blockquote>
[!Note]<br />
La faute d’orthographe dans le nom de la propriété se trouve dans la version finale du contrôle.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Dens</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la compression est activée.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le mode plein écran géré par le conteneur est activé.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si l’imprimante et la redirection du presse-papiers sont activées.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Spécifie le nom du fichier contenant les données d’icône qui seront accessibles lors de l’affichage du client en mode plein écran.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IndexIcône</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Spécifie l’index de l’icône dans le fichier icône actuel.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Spécifie les noms des dll clientes du canal virtuel à charger.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

