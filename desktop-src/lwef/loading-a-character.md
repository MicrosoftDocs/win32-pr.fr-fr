---
title: Chargement d’un caractère
description: Chargement d’un caractère
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673118"
---
# <a name="loading-a-character"></a><span data-ttu-id="4162a-103">Chargement d’un caractère</span><span class="sxs-lookup"><span data-stu-id="4162a-103">Loading a Character</span></span>

<span data-ttu-id="4162a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4162a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4162a-105">Pour animer un caractère, vous devez d’abord charger le caractère.</span><span class="sxs-lookup"><span data-stu-id="4162a-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="4162a-106">Utilisez la méthode [**Load**](load-method.md) pour charger les données du caractère.</span><span class="sxs-lookup"><span data-stu-id="4162a-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="4162a-107">Microsoft agent prend en charge deux formats de données de caractères et d’animation : un seul fichier structuré et des fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="4162a-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="4162a-108">En général, vous utilisez le format de fichier unique (. ACS) lorsque les données sont stockées localement.</span><span class="sxs-lookup"><span data-stu-id="4162a-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="4162a-109">Le format de fichier multiple (. ACF,. CCN) fonctionne mieux lorsque vous souhaitez télécharger des animations individuellement, par exemple lors de l’accès à des animations à partir d’un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="4162a-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="4162a-110">Une application cliente ne peut charger qu’une seule instance du même caractère.</span><span class="sxs-lookup"><span data-stu-id="4162a-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="4162a-111">Toute tentative de chargement du même caractère plusieurs fois échoue.</span><span class="sxs-lookup"><span data-stu-id="4162a-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="4162a-112">Toutefois, une application peut avoir plusieurs instances du même caractère chargées en fournissant des connexions distinctes à Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4162a-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="4162a-113">Par exemple, une application peut charger le même caractère à partir de deux copies du contrôle Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4162a-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="4162a-114">Vous pouvez également définir vos propres caractères en vue de les utiliser avec Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4162a-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="4162a-115">Vous pouvez utiliser n’importe quel outil de rendu que vous préférez créer les images, à condition de vous retrouver avec les fichiers de format bitmap Windows.</span><span class="sxs-lookup"><span data-stu-id="4162a-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="4162a-116">Pour assembler et compiler les images d’un caractère dans des animations en vue de les utiliser avec Microsoft Agent, utilisez l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4162a-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4162a-117">Cet outil vous permet de définir les propriétés par défaut d’un caractère et de définir des animations pour ce caractère.</span><span class="sxs-lookup"><span data-stu-id="4162a-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="4162a-118">L’éditeur de caractères Microsoft agent vous permet également de sélectionner le format de fichier approprié lorsque vous créez un caractère.</span><span class="sxs-lookup"><span data-stu-id="4162a-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




