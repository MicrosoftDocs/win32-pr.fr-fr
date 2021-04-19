---
title: Classe Win32_WinSAT
description: Définit des informations d’évaluation récapitulatives pour l’évaluation formelle la plus récente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Classe Win32_WinSAT WinSAT
- Win32_WinSAT classe WinSAT, décrite
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511601"
---
# <a name="win32_winsat-class"></a>\_Classe Win32 WinSAT

\[**Win32 \_ WinSAT** peut être modifié ou non disponible pour les mises en production après Windows 8.1.\]

Définit des informations d’évaluation récapitulatives pour l’évaluation formelle la plus récente.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ WinSAT** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ WinSAT** possède ces propriétés.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Un score pour les processeurs sur l’ordinateur.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Après Windows 8.1, WinSAT n’évalue plus les fonctionnalités graphiques à trois dimensions (jeux) de l’ordinateur et la capacité du pilote Graphics à afficher des objets et à exécuter des nuanceurs à l’aide de cette évaluation. Pour la compatibilité, les valeurs Sentinel des rapports WinSAT pour les métriques et les scores, toutefois, ne sont pas calculées en temps réel.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Un score pour le débit de lecture séquentielle sur le disque dur principal sur l’ordinateur.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Score pour les capacités graphiques de l’ordinateur.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Un score pour le débit et la capacité de la mémoire de l’ordinateur.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Cette propriété doit être définie sur « MostRecentAssessment » dans la clause WHERE de votre requête WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de l’évaluation. Pour obtenir une description des valeurs possibles, consultez l’énumération de l' [**\_ \_ État d’évaluation WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valide** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valide** (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Score de base pour l’ordinateur. Pour plus d’informations sur la valeur du score, consultez la propriété [**IProvideWinSATResultsInfo :: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur les scores des sous-composants, tels que **MemoryScore**, consultez la propriété [**IProvideWinSATAssessmentInfo :: score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple qui montre comment utiliser WMI pour récupérer des données de cette classe, consultez la méthode [**IProvideWinSATVisuals :: obtenir une \_ bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





