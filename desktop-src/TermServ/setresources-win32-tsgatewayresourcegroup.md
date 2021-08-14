---
title: Méthode SetResources de la classe Win32_TSGatewayResourceGroup
description: Définit la propriété des ressources pour ce groupe de ressources.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetResources
- Services Bureau à distance de la méthode SetResources, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode SetResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f357b08e554c5fa97cc26d15c52e65a0668512eeef20bceeba8d194510bdf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987669"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Méthode SetResources de la \_ classe Win32 TSGatewayResourceGroup

Définit la propriété des **ressources** pour ce groupe de ressources.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ressources* \[ dans\]
</dt> <dd>

Liste de ressources séparées par des points-virgules dans ce groupe de ressources. « \* » Signifie toutes les ressources.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.

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

 

