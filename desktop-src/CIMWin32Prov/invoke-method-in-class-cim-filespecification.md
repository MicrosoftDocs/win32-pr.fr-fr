---
description: La méthode Invoke de la \_ classe CIM FileSpecification évalue une vérification particulière. Les détails sur la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de vérification CIM non abstraites \_ . Cette méthode est héritée de la \_ vérification CIM.
ms.assetid: cefb64b5-c06f-4775-a903-4e8a8b99a6ae
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f76b93c890b0b36eb07cb3e7ec4a3248d1f9bf49d4fcf2777d2239572b000342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064949"
---
# <a name="invoke-method-of-the-cim_filespecification-class"></a>Méthode Invoke de la \_ classe CIM FileSpecification

La méthode **Invoke** de la classe [**CIM \_ FileSpecification**](cim-filespecification.md) évalue une vérification particulière. Les détails sur la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de [**\_ vérification CIM**](cim-check.md) non abstraites. Cette méthode est héritée de la **\_ vérification CIM**.

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

Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.

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

[\_FILESPECIFICATION CIM](invoke-method-in-class-cim-filespecification.md)
</dt> <dt>

[**\_FILESPECIFICATION CIM**](cim-filespecification.md)
</dt> </dl>

 

