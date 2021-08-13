---
description: La méthode Invoke de la \_ classe CIM CopyFileAction prend une mesure particulière. Les détails sur la façon dont la méthode effectue l’action sont spécifiques à l’implémentation. Cette méthode est héritée de l' \_ action CIM.
ms.assetid: b948e9ed-332d-4ac5-be7f-88b7f46f5f1d
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_CopyFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 66b3e66db91be28eb16d92266bc7ab4acba0de56ede57da1b6c375ee91de5adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675760"
---
# <a name="invoke-method-of-the-cim_copyfileaction-class"></a>Méthode Invoke de la \_ classe CIM CopyFileAction

La méthode **Invoke** de la classe [**CIM \_ CopyFileAction**](cim-copyfileaction.md) prend une mesure particulière. Les détails sur la façon dont la méthode effectue l’action sont spécifiques à l’implémentation. Cette méthode est héritée de l' [**\_ action CIM**](cim-action.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

## <a name="remarks"></a>Remarques

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_COPYFILEACTION CIM**](invoke-method-in-class-cim-copyfileaction.md)
</dt> <dt>

[**\_COPYFILEACTION CIM**](cim-copyfileaction.md)
</dt> </dl>

 

