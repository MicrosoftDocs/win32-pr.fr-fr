---
description: Les programmeurs utilisent des technologies d’autorisation pour créer des logiciels de contrôle d’accès, le contrôle d’accès à Internet, le contrôle d’accès de sécurité et la sécurité des fichiers.
ms.assetid: 1b8306da-7577-40b8-b77c-5762c1962f00
title: Autorisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c939a4dd8747b7219fe99650ab7a078239b5f643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211089"
---
# <a name="authorization"></a><span data-ttu-id="3c0f4-103">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0f4-103">Authorization</span></span>

## <a name="purpose"></a><span data-ttu-id="3c0f4-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="3c0f4-104">Purpose</span></span>

<span data-ttu-id="3c0f4-105">L’autorisation est le droit accordé à un individu d’utiliser le système et les données qui y sont stockées.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-105">Authorization is the right granted an individual to use the system and the data stored on it.</span></span> <span data-ttu-id="3c0f4-106">L’autorisation est généralement configurée par un administrateur système et vérifiée par l’ordinateur en fonction d’une forme d’identification utilisateur, telle qu’un numéro de code ou un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-106">Authorization is typically set up by a system administrator and verified by the computer based on some form of user identification, such as a code number or password.</span></span>

<span data-ttu-id="3c0f4-107">Les technologies d’autorisation Microsoft incluent le gestionnaire d’autorisations et l’API auth.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-107">Microsoft authorization technologies include Authorization Manager and the Authz API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3c0f4-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="3c0f4-108">Developer audience</span></span>

<span data-ttu-id="3c0f4-109">Les technologies d’autorisation Microsoft sont destinées à être utilisées par les développeurs d’applications basées sur les systèmes d’exploitation Windows Server et Windows qui contrôlent l’accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-109">Microsoft authorization technologies are intended for use by developers of applications based on the Windows Server and Windows operating systems that control access to resources.</span></span> <span data-ttu-id="3c0f4-110">Les développeurs doivent être familiarisés avec la programmation basée sur Windows.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="3c0f4-111">Bien que cela ne soit pas obligatoire, il est recommandé de comprendre les sujets relatifs à l’autorisation ou à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-111">Although not required, an understanding of authorization or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3c0f4-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="3c0f4-112">Run-time requirements</span></span>

<span data-ttu-id="3c0f4-113">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c0f4-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3c0f4-114">In this section</span></span>



| <span data-ttu-id="3c0f4-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3c0f4-115">Topic</span></span>                                                             | <span data-ttu-id="3c0f4-116">Description</span><span class="sxs-lookup"><span data-stu-id="3c0f4-116">Description</span></span>                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c0f4-117">À propos de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0f4-117">About Authorization</span></span>](about-authorization.md)<br/>         | <span data-ttu-id="3c0f4-118">Concepts d’autorisation clés et une vue de haut niveau des technologies d’autorisation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-118">Key authorization concepts and a high-level view of Microsoft authorization technologies.</span></span><br/>                                                                                                                                                                                  |
| <span data-ttu-id="3c0f4-119">Utilisation de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0f4-119">Using Authorization</span></span><br/>                                    | <span data-ttu-id="3c0f4-120">Processus d’autorisation, procédures et exemples de programmes utilisant les technologies d’autorisation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-120">Authorization processes, procedures, and examples of programs using Microsoft authorization technologies.</span></span> <span data-ttu-id="3c0f4-121">Ces informations sont présentées dans les sections utilisation des langages de programmation [C++](using-authorization-in-c--.md) et [script](using-authorization-in-script.md) .</span><span class="sxs-lookup"><span data-stu-id="3c0f4-121">This information is presented in using sections for [C++](using-authorization-in-c--.md) and [Script](using-authorization-in-script.md) programming languages.</span></span><br/> |
| [<span data-ttu-id="3c0f4-122">Référence d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0f4-122">Authorization Reference</span></span>](authorization-reference.md)<br/> | <span data-ttu-id="3c0f4-123">Informations détaillées sur les fonctions d’autorisation, les interfaces, les structures et d’autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-123">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                                                                                                                                                                |



 

 

 




