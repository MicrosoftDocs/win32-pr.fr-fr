---
title: Écriture de flux de vitesse binaire variable
description: Écriture de flux de vitesse binaire variable
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), écriture de flux VBR
- ASF (Advanced Systems Format), écriture de flux VBR
- Vitesse de transmission variable (VBR), écriture de flux
- VBR (vitesse de transmission variable), écriture de flux
- flux, écriture VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723394"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="f2a92-108">Écriture de flux de vitesse binaire variable</span><span class="sxs-lookup"><span data-stu-id="f2a92-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="f2a92-109">Les flux à débit binaire variable (VBR) sont écrits de la même façon que les flux à débit binaire constant (CBR).</span><span class="sxs-lookup"><span data-stu-id="f2a92-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="f2a92-110">La seule différence réside dans le traitement effectué en interne par le writer et les codecs.</span><span class="sxs-lookup"><span data-stu-id="f2a92-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="f2a92-111">Toutefois, le VBR basé sur la vitesse binaire (à la fois contraint et sans contrainte) requiert une passe de prétraitement dans le writer.</span><span class="sxs-lookup"><span data-stu-id="f2a92-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="f2a92-112">Vous devez vérifier la valeur de retour pour le premier appel que vous apportez à [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="f2a92-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="f2a92-113">Si le code d’erreur retourné est NS \_ E \_ nombre de passes non valides \_ \_ , le flux requiert une passe de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="f2a92-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2a92-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2a92-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2a92-115">**Utilisation de l’encodage Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="f2a92-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="f2a92-116">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="f2a92-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




