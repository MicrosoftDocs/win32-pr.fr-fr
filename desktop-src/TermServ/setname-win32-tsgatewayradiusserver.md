---
title: Méthode SetName de la classe Win32_TSGatewayRADIUSServer
description: Définit la propriété de nom de ce serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetName
- Services Bureau à distance de la méthode SetName, classe Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, méthode SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4b563c59ce1546b4cf471653407e3390676625
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222001"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a>Méthode SetName de la \_ classe Win32 TSGatewayRADIUSServer

Définit la propriété de **nom** de ce serveur protocole RADIUS (Remote Authentication Dial-in User Service) (RADIUS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nouveau nom.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

