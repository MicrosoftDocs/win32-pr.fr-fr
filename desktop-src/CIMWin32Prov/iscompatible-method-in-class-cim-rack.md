---
description: Vérifie si le rack référencé peut être contenu ou inséré dans le package physique.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Méthode IsCompatible de la classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3daf84cd47a89a53e808e73d4598c051b92e01197d4de18b43a5ce89ab9fb099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064497"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a>Méthode IsCompatible de la \_ classe de rack CIM

La méthode **IsCompatible** vérifie si le rack référencé peut être contenu ou inséré dans le package physique. Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode. Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** . Cette méthode est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ElementToCheck* \[ dans\]
</dt> <dd>

Référence à l’élément physique sur lequel cette méthode s’exécute.

</dd> </dl>

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

[**\_Rack CIM**](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[**\_Rack CIM**](cim-rack.md)
</dt> </dl>

 

