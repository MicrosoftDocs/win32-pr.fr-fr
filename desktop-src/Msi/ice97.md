---
description: ICE97 vérifie que deux composants n’isolent pas un composant partagé dans le même répertoire.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521247"
---
# <a name="ice97"></a><span data-ttu-id="d1096-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="d1096-103">ICE97</span></span>

<span data-ttu-id="d1096-104">ICE97 vérifie que deux composants n’isolent pas un composant partagé dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="d1096-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="d1096-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="d1096-105">Result</span></span>

<span data-ttu-id="d1096-106">ICE97 publie les avertissements suivants.</span><span class="sxs-lookup"><span data-stu-id="d1096-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="d1096-107">AVERTISSEMENT ICE97</span><span class="sxs-lookup"><span data-stu-id="d1096-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="d1096-108">Description</span><span class="sxs-lookup"><span data-stu-id="d1096-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d1096-109">Ce composant \[ 1 \] installe le composant partagé dans le même répertoire \[ 2 \] qu’un autre, ce qui interrompt les règles des composants si les deux composants (ou plus) sont sélectionnés pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1096-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="d1096-110">Deux composants ne doivent pas isoler un composant partagé dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="d1096-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="d1096-111">Par exemple, Composant1 et COMPONENT2, qui partagent ComponentShared, sont installés dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="d1096-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="d1096-112">Les deux spécifient ComponentShared comme un composant isolé.</span><span class="sxs-lookup"><span data-stu-id="d1096-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="d1096-113">En raison de l’isolation, les fichiers dans ComponentShared sont copiés deux fois dans la \_ référence de répertoire pour Composant1 et COMPONENT2.</span><span class="sxs-lookup"><span data-stu-id="d1096-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="d1096-114">Les composants disposent désormais d’un nombre de références sur la copie des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d1096-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="d1096-115">Il s’agit d’une violation des règles du composant d’installation.</span><span class="sxs-lookup"><span data-stu-id="d1096-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="d1096-116">Si Composant1 est désinstallé, les fichiers des composants isolés sont supprimés et COMPONENT2 est interrompu.</span><span class="sxs-lookup"><span data-stu-id="d1096-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1096-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1096-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1096-118">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="d1096-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



