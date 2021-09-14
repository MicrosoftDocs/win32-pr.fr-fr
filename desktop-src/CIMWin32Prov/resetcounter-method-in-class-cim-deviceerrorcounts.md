---
description: La méthode ResetCounter réinitialise les compteurs d’erreur et d’avertissement.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Méthode ResetCounter de la classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126858106"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>Méthode ResetCounter de la \_ classe CIM DeviceErrorCounts

La méthode **ResetCounter** réinitialise les compteurs d’erreur et d’avertissement. Une méthode est utilisée afin que l’instrumentation de l’appareil logique, qui calcule les erreurs et les avertissements, puisse également réinitialiser son traitement interne et ses compteurs. Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode. Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SelectedCounter* \[ dans\]
</dt> <dd>

Compteur d’erreurs à réinitialiser.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Tout** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Compteur d’erreurs indéterminé** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Compteur d’erreurs critiques** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Compteur d’erreurs majeures** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Compteur d’erreurs mineures** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Compteur d’avertissements** (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 (zéro) en cas de réussite, 1 (un) s’il n’est pas pris en charge et toute autre valeur si une erreur s’est produite.

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_DEVICEERRORCOUNTS CIM](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> </dl>

 

