---
UID: ''
title: LsaManageSidNameMapping fonction)
description: Ajoute ou supprime les mappages de SID/noms de l’ensemble de mappages inscrit auprès du service de recherche LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314492"
---
# <a name="lsamanagesidnamemapping-function"></a>LsaManageSidNameMapping fonction)

## <a name="description"></a>Description

La fonction **LsaManageSidNameMapping** ajoute ou supprime les mappages de sid/nom de l’ensemble de mappages inscrit auprès du service de recherche LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Paramètres

### <a name="optype-in"></a>OpType [in]

Indique si une fonction est appelée pour ajouter ou supprimer un mappage SID/nom.

### <a name="opinput-in"></a>OpInput [in]

Indique le domaine, le compte et les valeurs SID à utiliser au cours de cette opération. Des indicateurs supplémentaires peuvent également être définis dans cette structure.

### <a name="opoutput-out"></a>OpOutput [out]

Contient une valeur de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) qui indique la réussite ou l’échec de l’opération.

| Valeur | Signification |
|-------|---------|
| **Success** | L’opération est terminée sans erreur. |
| **NonMappingError** | Une erreur non liée au mappage de nom SID s’est produite. |
| **NameCollision** | Échec de l’opération en raison d’une collision de noms. |
| **SidCollision** | Échec de l’opération en raison d’une collision de SID. |
| **DomainNotFound** | Domaine correspondant introuvable. |
| **DomainSidPrefixMismatch** | Le SID fourni n’a pas le préfixe de domaine correct. |
| **MappingNotFound** | Mappage introuvable dans le cache. |

## <a name="returns"></a>Retours

Si le mappage est correctement inséré, la valeur de retour est STATUS_SUCCESS.
Sinon, si la fonction échoue en raison de conflits de noms ou de SID, STATUS_INVALID_PARAMETER erreur est retournée.

## <a name="remarks"></a>Notes

## <a name="see-also"></a>Voir aussi
