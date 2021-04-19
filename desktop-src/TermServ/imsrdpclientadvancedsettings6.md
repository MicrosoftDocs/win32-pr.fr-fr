---
title: Interface IMsRdpClientAdvancedSettings6
description: Expose les propriétés qui gèrent les paramètres de contrôle ActiveX avancés.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513798"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Interface IMsRdpClientAdvancedSettings6

Expose les propriétés qui gèrent les paramètres de contrôle ActiveX avancés. L’interface **IMsRdpClientAdvancedSettings6** est dérivée de l’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .

Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings6** à **QueryInterface**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientAdvancedSettings6** hérite de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md). **IMsRdpClientAdvancedSettings6** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientAdvancedSettings6** possède les propriétés suivantes.



| Propriété                                                                                                  | Type d’accès           | Description                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lecture/écriture<br/> | Spécifie le nom de principal du service (SPN) à utiliser pour l’authentification auprès du serveur.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Lecture seule<br/>  | Spécifie le type d’authentification utilisé pour cette connexion.<br/>                                                          |
| [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lecture/écriture<br/> | Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lecture/écriture<br/> | Spécifie si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lecture/écriture<br/> | Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + gauche.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lecture/écriture<br/> | Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + droite.<br/>         |
| [**PCB**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lecture/écriture<br/> | Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lecture/écriture<br/> | Spécifie si la souris doit utiliser le mode relatif.<br/>                                                                   |



 

## <a name="remarks"></a>Notes

Cette interface a été étendue par l’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , qui hérite de toutes les méthodes et propriétés des interfaces précédentes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

