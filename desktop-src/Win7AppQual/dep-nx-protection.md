---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protection DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868754"
---
# <a name="depnx-protection"></a><span data-ttu-id="d4229-103">Protection DEP/NX</span><span class="sxs-lookup"><span data-stu-id="d4229-103">DEP/NX Protection</span></span>

<span data-ttu-id="d4229-104">À compter de Windows Internet Explorer 7 sur Windows Vista, l’élément du panneau de configuration Internet comprend une option **activer la protection** de la mémoire pour atténuer les attaques en ligne.</span><span class="sxs-lookup"><span data-stu-id="d4229-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="d4229-105">Cette option est également appelée prévention de *l’exécution des données* (DEP) ou *No-Execute* (NX).</span><span class="sxs-lookup"><span data-stu-id="d4229-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="d4229-106">Quand cette option est activée, elle fonctionne avec le processeur pour empêcher les attaques par dépassement de mémoire tampon en bloquant l’exécution du code à partir de la mémoire qui est marquée comme non exécutable.</span><span class="sxs-lookup"><span data-stu-id="d4229-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="d4229-107">Dans Windows Internet Explorer 8 sur le système d’exploitation Windows Vista avec Service Pack 1 (SP1) ou une version ultérieure, cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4229-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="d4229-108">DEP/NX ne protège pas contre toutes les vulnérabilités basées sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d4229-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="d4229-109">Mais lorsqu’il est combiné à d’autres technologies telles que la randomisation du format d’espace d’adresse (ASLR), il permet d’éviter les vulnérabilités de dépassement de mémoire tampon courantes dans Windows Internet Explorer et les modules complémentaires qu’il charge.</span><span class="sxs-lookup"><span data-stu-id="d4229-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="d4229-110">Aucune intervention supplémentaire de l’utilisateur n’est requise pour fournir cette protection et aucune nouvelle invite n’est introduite.</span><span class="sxs-lookup"><span data-stu-id="d4229-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4229-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4229-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4229-112">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="d4229-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



