---
description: Journalisation des erreurs
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745972"
---
# <a name="logging-errors"></a><span data-ttu-id="17b65-103">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="17b65-103">Logging Errors</span></span>

<span data-ttu-id="17b65-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="17b65-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="17b65-105">Les [services de modification DirectShow](directshow-editing-services.md) (des) fournissent un mécanisme intégré pour la journalisation des erreurs qui se produisent lors du chargement, de la construction ou du rendu d’un projet des.</span><span class="sxs-lookup"><span data-stu-id="17b65-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="17b65-106">Cet article présente un exemple d’application console qui charge un fichier de projet XML et tente de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="17b65-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="17b65-107">Si une erreur se produit, l’application imprime un message d’erreur dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="17b65-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="17b65-108">L’exemple de code présenté dans cet article s’appuie sur l’exemple donné lors [du chargement et de l’aperçu d’un projet](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="17b65-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="17b65-109">Votre application n’est pas obligée d’implémenter la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="17b65-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="17b65-110">DES n’enregistre pas d’erreurs, sauf si vous le demandez explicitement.</span><span class="sxs-lookup"><span data-stu-id="17b65-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="17b65-111">Cet article suppose que vous comprenez la programmation du client COM et le modèle de chronologie DES.</span><span class="sxs-lookup"><span data-stu-id="17b65-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="17b65-112">En outre, vous devez comprendre les principes fondamentaux de la programmation d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="17b65-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="17b65-113">Pour plus d’informations sur les chronologies dans DES, consultez [le modèle Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="17b65-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="17b65-114">Cet article contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="17b65-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="17b65-115">Vue d’ensemble de la journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="17b65-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="17b65-116">Création d’une classe de journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="17b65-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="17b65-117">Implémentation de IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="17b65-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="17b65-118">Définition du journal des erreurs</span><span class="sxs-lookup"><span data-stu-id="17b65-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="17b65-119">Journal DES Erreurs DES : exemple de code</span><span class="sxs-lookup"><span data-stu-id="17b65-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="17b65-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17b65-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b65-121">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="17b65-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



