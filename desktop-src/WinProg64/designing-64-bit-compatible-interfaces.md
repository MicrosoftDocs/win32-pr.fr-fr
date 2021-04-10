---
title: Conception d’interfaces compatibles 64 bits
description: Des problèmes de compatibilité descendante se produisent lorsque vous ajoutez de nouveaux types de données ou méthodes à une interface, modifiez les anciens types de données ou utilisez des types de données de manière inappropriée.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilité descendante avec la programmation Windows 64 bits
- interfaces compatibles 64 bits programmation Windows 64 bits
- Guide de programmation Windows 64 bits, programmation Windows 64 bits, compatibilité
- compatibilité avec la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309946"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="aaa3e-107">Conception d’interfaces compatibles 64 bits</span><span class="sxs-lookup"><span data-stu-id="aaa3e-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="aaa3e-108">Le portage à partir de Windows 32 bits vers Windows 64 bits ne doit pas, en soi, créer des problèmes pour les applications distribuées, qu’ils utilisent des appels de procédure distante (RPC) directement ou via DCOM.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="aaa3e-109">Le modèle de programmation RPC spécifie des tailles de données bien définies et des types d’entiers de la même taille à chaque extrémité de la connexion.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="aaa3e-110">En outre, dans le modèle de données abstraites LLP64 développé pour Windows 64 bits, seuls les pointeurs sont étendus à 64 bits : tous les autres types de données Integer restent 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="aaa3e-111">Étant donné que les pointeurs sont locaux de chaque côté de la connexion client/serveur et sont généralement transmis en tant que marqueurs **null** ou non **null** , le moteur de marshaling peut gérer des tailles de pointeur différentes à la fin d’une connexion de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="aaa3e-112">Toutefois, des problèmes de compatibilité descendante se produisent lorsque vous ajoutez de nouveaux types de données ou de nouvelles méthodes à une interface, modifiez des types de données anciens ou utilisez des types de données de manière inappropriée.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="aaa3e-113">Les rubriques suivantes expliquent comment éviter ces situations (lorsque cela est possible) et comment concevoir des solutions de contournement robustes lorsqu’il n’est pas possible de les éviter.</span><span class="sxs-lookup"><span data-stu-id="aaa3e-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aaa3e-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="aaa3e-114">In this Section</span></span>

-   [<span data-ttu-id="aaa3e-115">Modification d’une interface existante</span><span class="sxs-lookup"><span data-stu-id="aaa3e-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="aaa3e-116">Éviter le masquage des informations</span><span class="sxs-lookup"><span data-stu-id="aaa3e-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="aaa3e-117">Éviter le polymorphisme</span><span class="sxs-lookup"><span data-stu-id="aaa3e-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="aaa3e-118">Utilisation de nouveaux types de données dans votre fichier IDL</span><span class="sxs-lookup"><span data-stu-id="aaa3e-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="aaa3e-119">Préparation de votre application pour Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="aaa3e-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="aaa3e-120">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="aaa3e-120">Related Sections</span></span>

<span data-ttu-id="aaa3e-121">Si vous n’êtes pas déjà familiarisé avec les nouveaux types de données, l’environnement de travail et les modifications d’API pour Windows 64 bits, consultez [préparation pour windows 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="aaa3e-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




