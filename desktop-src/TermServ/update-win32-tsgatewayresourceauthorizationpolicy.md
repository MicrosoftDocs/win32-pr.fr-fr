---
title: Méthode Update de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Met à jour la stratégie d’autorisation des ressources Bureau à distance actuelle (RD \ 160 ; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Mettre à jour la méthode Services Bureau à distance
- Mise à jour de la méthode Services Bureau à distance, classe Win32_TSGatewayResourceAuthorizationPolicy
- Services Bureau à distance de la classe Win32_TSGatewayResourceAuthorizationPolicy, méthode Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104281"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode Update de la \_ classe TSGatewayResourceAuthorizationPolicy Win32

Met à jour la stratégie d’autorisation d’accès aux ressources Bureau à distance en cours (RD RAP).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom de la RD RAP.

</dd> <dt>

*Description* \[ dans\]
</dt> <dd>

Description de la RD RAP.

</dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Indique si le RAP des services Bureau à distance doit être activé.

</dd> <dt>

*ResourceGroupName* \[ dans\]
</dt> <dd>

Nom du groupe de ressources associé à ce RAP.

</dd> <dt>

*ResourceGroupType* \[ dans\]
</dt> <dd>

Type de groupe de ressources.

<dt>

ROUTAGE
</dt> <dd>

Groupe de ressources.

</dd> <dt>

CG
</dt> <dd>

Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.

</dd> <dt>

TOUS les
</dt> <dd>

Toutes les ressources.

</dd> </dl> </dd> <dt>

*UserGroupNames* \[ dans\]
</dt> <dd>

Liste de noms de groupes d’utilisateurs séparés par des points-virgules. Les noms sont au format *domaine \\ UserGroupName*. Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé.

</dd> <dt>

*ProtocolNames* \[ dans\]
</dt> <dd>

Liste délimitée par des points-virgules des noms de protocole qui sont activés pour cette stratégie. Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*PortNumbers* \[ dans\]
</dt> <dd>

Liste délimitée par des points-virgules des numéros de port activés pour cette stratégie. Pour autoriser n’importe quel numéro de port, définissez « \* ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

