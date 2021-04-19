---
UID: ''
title: GuardCheckLongJumpTarget fonction)
description: Tente de vérifier si la cible d’un longjmp est valide.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106543615"
---
# <a name="guardchecklongjumptarget-function"></a>GuardCheckLongJumpTarget fonction)

## <a name="description"></a>Description

Tente de vérifier si la cible d’un [longjmp](/cpp/c-runtime-library/reference/longjmp) est valide pour un processus pour lequel la [protection du workflow de contrôle (cfg)](../secbp/control-flow-guard.md) est activée.

Si l’adresse cible correspond à un mappage d’image, les cibles valides sont extraites pour le binaire.
La fonction utilise ces cibles pour valider la cible.
Si le fichier binaire ne contient pas de métadonnées décrivant le jeu de cibles *longjmp* valides, la fonction retourne la **valeur true**.

Si l’adresse cible correspond à un mappage de non-image, comme dans le code JIT, une stratégie globale en lecture seule est consultée pour déterminer si le saut est autorisé.

## <a name="parameters"></a>Paramètres

### <a name="targetaddress-in"></a>TargetAddress [in]

Adresse cible du saut.

### <a name="flags-in"></a>Flags [in]

Indicateurs décrivant l’opération à effectuer sur l’adresse.
Si vous spécifiez **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), cette fonction ne met pas fin au processus si la cible n’est pas valide.

## <a name="returns"></a>Retours

**True** si la cible est valide ; sinon, **false**.

## <a name="remarks"></a>Notes

## <a name="see-also"></a>Voir aussi
