---
title: Comprendre Direct3D 12
description: Pour écrire des jeux et des applications en 3D pour Windows 10 et Windows 10 mobile, vous devez comprendre les principes fondamentaux de la technologie Direct3D 12 et comment vous préparer à l’utiliser dans vos jeux et vos applications.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548605"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="b7561-103">Comprendre Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b7561-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="b7561-104">Pour écrire des jeux et des applications en 3D pour Windows 10 et Windows 10 mobile, vous devez comprendre les principes fondamentaux de la technologie Direct3D 12 et comment vous préparer à l’utiliser dans vos jeux et vos applications.</span><span class="sxs-lookup"><span data-stu-id="b7561-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="b7561-105">Utilisez les rubriques de cette section pour installer et découvrir l’environnement dans lequel vous allez programmer vos applications et vos jeux avec Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b7561-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="b7561-106">Ce contenu vous aidera également à porter vos applications et vos jeux Direct3D 11 vers Direct3D 12, afin que vous puissiez tirer parti des fonctionnalités et de l’efficacité de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b7561-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="b7561-107">Pour programmer avec Direct3D 12, vous avez besoin des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="b7561-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="b7561-108">Une plateforme matérielle avec un GPU compatible Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b7561-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="b7561-109">[Afficher les pilotes](/previous-versions//ff569172(v=vs.85)) qui prennent en charge le modèle WDDM (Windows Display Driver Model) 2,0</span><span class="sxs-lookup"><span data-stu-id="b7561-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7561-110">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b7561-110">In this section</span></span>



| <span data-ttu-id="b7561-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b7561-111">Topic</span></span>                                                                                                               | <span data-ttu-id="b7561-112">Description</span><span class="sxs-lookup"><span data-stu-id="b7561-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7561-113">Configuration de l’environnement de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b7561-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="b7561-114">Décrit l’installation, les outils et les bibliothèques prises en charge qui constituent un environnement de développement Direct3D 12 productif.</span><span class="sxs-lookup"><span data-stu-id="b7561-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="b7561-115">Création d’un composant Direct3D 12 de base</span><span class="sxs-lookup"><span data-stu-id="b7561-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="b7561-116">Cette rubrique décrit le déroulement des appels pour créer un composant Direct3D 12 de base.</span><span class="sxs-lookup"><span data-stu-id="b7561-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="b7561-117">Modifications importantes de Direct3D 11 à Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b7561-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="b7561-118">Direct3D 12 représente un écart significatif par rapport au modèle de programmation Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b7561-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="b7561-119">Direct3D 12 permet aux applications d’être plus proches du matériel que jamais.</span><span class="sxs-lookup"><span data-stu-id="b7561-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="b7561-120">Niveaux de fonctionnalité matérielle</span><span class="sxs-lookup"><span data-stu-id="b7561-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="b7561-121">Décrit les fonctionnalités des niveaux de \_ fonctionnalité matérielle de 11 0 à 12 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="b7561-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="b7561-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7561-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7561-123">Guide de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b7561-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

