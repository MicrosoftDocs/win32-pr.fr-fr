---
title: ActivationFailureLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les demandes ayant échoué pour le lancement et l’activation des composants.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valeur de Registre ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380385"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="a4050-104">ActivationFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="a4050-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="a4050-105">Définit le niveau de détail des entrées du journal des événements sur les demandes ayant échoué pour le lancement et l’activation des composants.</span><span class="sxs-lookup"><span data-stu-id="a4050-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a4050-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="a4050-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="a4050-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a4050-107">Remarks</span></span>

<span data-ttu-id="a4050-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a4050-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="a4050-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4050-109">Value</span></span> | <span data-ttu-id="a4050-110">Description</span><span class="sxs-lookup"><span data-stu-id="a4050-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4050-111">0</span><span class="sxs-lookup"><span data-stu-id="a4050-111">0</span></span>     | <span data-ttu-id="a4050-112">Utilisez la journalisation discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="a4050-112">Use discretionary logging.</span></span> <span data-ttu-id="a4050-113">Consignez les échecs par défaut, mais les clients peuvent remplacer ce comportement en spécifiant CLSCTX \_ aucun \_ \_ Journal des échecs dans [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span><span class="sxs-lookup"><span data-stu-id="a4050-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="a4050-114">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a4050-114">This is the default value.</span></span> |
| <span data-ttu-id="a4050-115">1</span><span class="sxs-lookup"><span data-stu-id="a4050-115">1</span></span>     | <span data-ttu-id="a4050-116">Consigne toujours toutes les défaillances, quel que soit le client spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4050-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a4050-117">2</span><span class="sxs-lookup"><span data-stu-id="a4050-117">2</span></span>     | <span data-ttu-id="a4050-118">Ne consignez jamais les échecs, quels que soient les éléments spécifiés par le client.</span><span class="sxs-lookup"><span data-stu-id="a4050-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="a4050-119">Si vous avez besoin d’une application pour contrôler la journalisation des événements, il est recommandé de définir cette valeur sur 0 et d’écrire le code client pour la remplacer si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a4050-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="a4050-120">Il est vivement recommandé de ne pas définir la valeur sur 2.</span><span class="sxs-lookup"><span data-stu-id="a4050-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="a4050-121">Si la journalisation des événements est désactivée, il est plus difficile de diagnostiquer les problèmes.</span><span class="sxs-lookup"><span data-stu-id="a4050-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="a4050-122">Pour les échecs d’autorisation de restrictions d’ordinateur, où COM n’a pas de CLSCTX bits, COM traite une valeur de 0 comme 1.</span><span class="sxs-lookup"><span data-stu-id="a4050-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4050-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4050-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4050-124">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="a4050-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




