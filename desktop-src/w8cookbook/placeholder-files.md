---
title: Fichiers d’espace réservé
description: Fichiers d’espace réservé
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "106531607"
---
# <a name="placeholder-files"></a><span data-ttu-id="99ac3-103">Fichiers d’espace réservé</span><span class="sxs-lookup"><span data-stu-id="99ac3-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="99ac3-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="99ac3-104">Platform</span></span>

<span data-ttu-id="99ac3-105">**Clients-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="99ac3-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="99ac3-106">**Serveurs-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="99ac3-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="99ac3-107">Description</span><span class="sxs-lookup"><span data-stu-id="99ac3-107">Description</span></span>

<span data-ttu-id="99ac3-108">Les fichiers d’espace réservé permettent aux utilisateurs d’afficher et de gérer les fichiers Microsoft OneDrive, quelle que soit la connectivité.</span><span class="sxs-lookup"><span data-stu-id="99ac3-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="99ac3-109">Les fichiers d’espace réservé représentent l’espace de noms OneDrive, même lorsque les fichiers ne sont pas mis en cache localement.</span><span class="sxs-lookup"><span data-stu-id="99ac3-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="99ac3-110">Ils contiennent des métadonnées de fichier et des images miniatures de photos.</span><span class="sxs-lookup"><span data-stu-id="99ac3-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="99ac3-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="99ac3-111">Manifestation</span></span>

<span data-ttu-id="99ac3-112">Pour les utilisateurs finaux et les développeurs, les fichiers d’espace réservé s’affichent et se comportent quasiment de la même façon que les fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="99ac3-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="99ac3-113">Si votre application utilise la boîte de dialogue de fichier commune pour énumérer le système de fichiers, votre application n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="99ac3-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="99ac3-114">Quand l’utilisateur tente d’ouvrir le fichier à partir de la boîte de dialogue commune/file, le contenu du fichier est téléchargé et est transmis à votre application.</span><span class="sxs-lookup"><span data-stu-id="99ac3-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="99ac3-115">Si votre application accède directement au système de fichiers, votre application peut tirer parti des fichiers d’espace réservé à l’aide des instructions ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="99ac3-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="99ac3-116">Solution</span><span class="sxs-lookup"><span data-stu-id="99ac3-116">Solution</span></span>

-   <span data-ttu-id="99ac3-117">Les espaces réservés sont masqués par Convention en fonction des attributs</span><span class="sxs-lookup"><span data-stu-id="99ac3-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="99ac3-118">Identifier les espaces réservés à l’aide de la balise d’analyse ID d’analyse d’analyse d’e/s \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="99ac3-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="99ac3-119">Utilisez le modèle de données Shell pour un comportement transparent :</span><span class="sxs-lookup"><span data-stu-id="99ac3-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="99ac3-120">Utiliser SHCreateItemFromParsingName () pour créer un élément de Shell</span><span class="sxs-lookup"><span data-stu-id="99ac3-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="99ac3-121">Liaison au flux à l’aide de IShellItem :: BindToHandler (BHID \_ Stream)</span><span class="sxs-lookup"><span data-stu-id="99ac3-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="99ac3-122">Gestionnaire de propriétés utilisateur pour l’accès aux propriétés (IShellItem2 :: GetPropertyHandler)</span><span class="sxs-lookup"><span data-stu-id="99ac3-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="99ac3-123">Thumbnailhandler de l’interface utilisateur pour obtenir des images miniatures pour les espaces réservés</span><span class="sxs-lookup"><span data-stu-id="99ac3-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="99ac3-124">Spécifiez SupportedProtocols = \* sur votre implémentation de verbe si le verbe est lié au flux via BindToHandler</span><span class="sxs-lookup"><span data-stu-id="99ac3-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




