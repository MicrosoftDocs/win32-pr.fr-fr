---
title: Méthode RemoveResources de la classe Win32_TSGatewayResourceGroup
description: Supprime les ressources du groupe de ressources.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveResources
- Services Bureau à distance de la méthode RemoveResources, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385259"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Méthode RemoveResources de la \_ classe Win32 TSGatewayResourceGroup

Supprime les ressources du groupe de ressources.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ressources* \[ dans\]
</dt> <dd>

Liste de ressources séparées par des points-virgules à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.

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

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

