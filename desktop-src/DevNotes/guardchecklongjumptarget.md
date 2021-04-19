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
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="f2e96-103">GuardCheckLongJumpTarget fonction)</span><span class="sxs-lookup"><span data-stu-id="f2e96-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="f2e96-104">Description</span><span class="sxs-lookup"><span data-stu-id="f2e96-104">Description</span></span>

<span data-ttu-id="f2e96-105">Tente de vérifier si la cible d’un [longjmp](/cpp/c-runtime-library/reference/longjmp) est valide pour un processus pour lequel la [protection du workflow de contrôle (cfg)](../secbp/control-flow-guard.md) est activée.</span><span class="sxs-lookup"><span data-stu-id="f2e96-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="f2e96-106">Si l’adresse cible correspond à un mappage d’image, les cibles valides sont extraites pour le binaire.</span><span class="sxs-lookup"><span data-stu-id="f2e96-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="f2e96-107">La fonction utilise ces cibles pour valider la cible.</span><span class="sxs-lookup"><span data-stu-id="f2e96-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="f2e96-108">Si le fichier binaire ne contient pas de métadonnées décrivant le jeu de cibles *longjmp* valides, la fonction retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f2e96-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="f2e96-109">Si l’adresse cible correspond à un mappage de non-image, comme dans le code JIT, une stratégie globale en lecture seule est consultée pour déterminer si le saut est autorisé.</span><span class="sxs-lookup"><span data-stu-id="f2e96-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2e96-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2e96-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="f2e96-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="f2e96-111">TargetAddress [in]</span></span>

<span data-ttu-id="f2e96-112">Adresse cible du saut.</span><span class="sxs-lookup"><span data-stu-id="f2e96-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="f2e96-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="f2e96-113">Flags [in]</span></span>

<span data-ttu-id="f2e96-114">Indicateurs décrivant l’opération à effectuer sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f2e96-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="f2e96-115">Si vous spécifiez **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), cette fonction ne met pas fin au processus si la cible n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f2e96-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="f2e96-116">Retours</span><span class="sxs-lookup"><span data-stu-id="f2e96-116">Returns</span></span>

<span data-ttu-id="f2e96-117">**True** si la cible est valide ; sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="f2e96-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e96-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f2e96-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="f2e96-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2e96-119">See also</span></span>
