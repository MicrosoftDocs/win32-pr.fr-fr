---
description: La méthode Invoke de la \_ classe CIM SettingCheck évalue une vérification particulière. Les détails de la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de vérification CIM non abstraites \_ . Cette méthode est héritée de la \_ vérification CIM.
ms.assetid: b2a9baea-cc5c-43d9-a93c-e3a77823d705
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8c10246e841182aff1b49742694eeb3871d7862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950552"
---
# <a name="invoke-method-of-the-cim_settingcheck-class"></a>Méthode Invoke de la \_ classe CIM SettingCheck

La méthode **Invoke** de la classe [**CIM \_ SettingCheck**](cim-settingcheck.md) évalue une vérification particulière. Les détails de la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de [**\_ vérification CIM**](cim-check.md) non abstraites. Cette méthode est héritée de la **\_ vérification CIM**.

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

## <a name="remarks"></a>Notes

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

[\_SETTINGCHECK CIM](invoke-method-in-class-cim-settingcheck.md)
</dt> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> </dl>

 

