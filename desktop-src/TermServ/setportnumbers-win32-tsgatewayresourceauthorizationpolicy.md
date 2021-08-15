---
title: Méthode SetPortNumbers de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit les numéros de port qui sont autorisés à se connecter à la ressource par le biais de Bureau à distance passerelle (passerelle des services Bureau à distance).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPortNumbers
- Services Bureau à distance de la méthode SetPortNumbers, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c151302abfda0b6bc42566770c0e8b8fb10dbab789cf2ece886be557efb023e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987769"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode SetPortNumbers de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Définit les numéros de port qui sont autorisés à se connecter à la ressource par le biais de Bureau à distance passerelle (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PortNumbers* \[ dans\]
</dt> <dd>

Liste des numéros de port séparés par des points-virgules autorisés pour cette stratégie d’autorisation des ressources Bureau à distance (RD RAP). Pour autoriser n’importe quel numéro de port, définissez « \* ».

</dd> </dl>

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

