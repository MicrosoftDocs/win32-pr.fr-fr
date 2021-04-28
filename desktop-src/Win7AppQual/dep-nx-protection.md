---
description: Protection DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protection DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088567"
---
# <a name="depnx-protection"></a><span data-ttu-id="33207-103">Protection DEP/NX</span><span class="sxs-lookup"><span data-stu-id="33207-103">DEP/NX Protection</span></span>

<span data-ttu-id="33207-104">À compter de Windows Internet Explorer 7 sur Windows Vista, l’élément du panneau de configuration Internet comprend une option **activer la protection** de la mémoire pour atténuer les attaques en ligne.</span><span class="sxs-lookup"><span data-stu-id="33207-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="33207-105">Cette option est également appelée prévention de *l’exécution des données* (DEP) ou *No-Execute* (NX).</span><span class="sxs-lookup"><span data-stu-id="33207-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="33207-106">Quand cette option est activée, elle fonctionne avec le processeur pour empêcher les attaques par dépassement de mémoire tampon en bloquant l’exécution du code à partir de la mémoire qui est marquée comme non exécutable.</span><span class="sxs-lookup"><span data-stu-id="33207-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="33207-107">Dans Windows Internet Explorer 8 sur le système d’exploitation Windows Vista avec Service Pack 1 (SP1) ou une version ultérieure, cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="33207-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="33207-108">DEP/NX ne protège pas contre toutes les vulnérabilités basées sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="33207-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="33207-109">Mais lorsqu’il est combiné à d’autres technologies telles que la randomisation du format d’espace d’adresse (ASLR), il permet d’éviter les vulnérabilités de dépassement de mémoire tampon courantes dans Windows Internet Explorer et les modules complémentaires qu’il charge.</span><span class="sxs-lookup"><span data-stu-id="33207-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="33207-110">Aucune intervention supplémentaire de l’utilisateur n’est requise pour fournir cette protection et aucune nouvelle invite n’est introduite.</span><span class="sxs-lookup"><span data-stu-id="33207-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33207-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33207-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33207-112">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="33207-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



