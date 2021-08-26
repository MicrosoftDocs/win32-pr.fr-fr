---
title: Créer une méthode de la classe Win32_TSGatewayResourceGroup
description: Crée un groupe de ressources.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayResourceGroup Class
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e4de66eff704ab5d061dcb7675c1ab4ef9d847e5e7235e872f5872b8f3376fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871749"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a>Créer une méthode de la \_ classe TSGatewayResourceGroup Win32

Crée un groupe de ressources.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom du groupe de ressources.

</dd> <dt>

*Description* \[ dans\]
</dt> <dd>

Description du groupe de ressources.

</dd> <dt>

*Ressources* \[ dans\]
</dt> <dd>

Liste de ressources séparées par des points-virgules dans ce groupe de ressources. « \* » Signifie toutes les ressources.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

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

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

