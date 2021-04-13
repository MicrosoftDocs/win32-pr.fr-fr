---
title: Monikers de fichiers
description: Monikers de fichiers
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309634"
---
# <a name="file-monikers"></a><span data-ttu-id="d53f9-103">Monikers de fichiers</span><span class="sxs-lookup"><span data-stu-id="d53f9-103">File Monikers</span></span>

<span data-ttu-id="d53f9-104">Les *monikers de fichiers* sont la classe moniker la plus simple.</span><span class="sxs-lookup"><span data-stu-id="d53f9-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="d53f9-105">Les monikers de fichiers peuvent être utilisés pour identifier tout objet stocké dans son propre fichier.</span><span class="sxs-lookup"><span data-stu-id="d53f9-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="d53f9-106">Un moniker de fichier agit comme un wrapper pour le nom de chemin d’accès que le système de fichiers natif affecte au fichier.</span><span class="sxs-lookup"><span data-stu-id="d53f9-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="d53f9-107">L’appel de [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) pour ce moniker provoquerait l’activation de cet objet, puis retournerait un pointeur d’interface vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="d53f9-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="d53f9-108">La source de l’objet nommé par le moniker doit fournir une implémentation de l’interface [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) pour prendre en charge la liaison d’un moniker de fichier.</span><span class="sxs-lookup"><span data-stu-id="d53f9-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="d53f9-109">Les monikers de fichiers peuvent représenter un chemin d’accès complet ou relatif.</span><span class="sxs-lookup"><span data-stu-id="d53f9-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="d53f9-110">Par exemple, le moniker de fichier pour un objet Spreadsheet stocké en tant que fichier C : \\ Work \\MySheet.xls contient des informations équivalentes à ce nom de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d53f9-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="d53f9-111">Toutefois, le moniker ne se compose pas nécessairement de la même chaîne.</span><span class="sxs-lookup"><span data-stu-id="d53f9-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="d53f9-112">La chaîne est simplement son *nom displayÂ*, une représentation du contenu du moniker qui est explicite pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d53f9-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="d53f9-113">Le nom complet, qui est disponible par le biais de la méthode [**IMoniker :: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , est utilisé uniquement lors de l’affichage d’un moniker pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d53f9-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="d53f9-114">Cette méthode obtient le nom complet de l’une des classes de moniker.</span><span class="sxs-lookup"><span data-stu-id="d53f9-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="d53f9-115">En interne, le moniker peut stocker les mêmes informations dans un format plus efficace pour effectuer des opérations de moniker, mais n’est pas significatif pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d53f9-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="d53f9-116">Ensuite, lorsque ce même objet est lié via un appel à la méthode [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , l’objet est activé, probablement en chargeant le fichier dans la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="d53f9-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="d53f9-117">OLE offre aux fournisseurs de monikers la fonction d’assistance [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) qui crée un objet moniker de fichier et retourne son pointeur au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d53f9-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d53f9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d53f9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d53f9-119">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="d53f9-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="d53f9-120">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="d53f9-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="d53f9-121">Monikers composites</span><span class="sxs-lookup"><span data-stu-id="d53f9-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="d53f9-122">Monikers d’élément</span><span class="sxs-lookup"><span data-stu-id="d53f9-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="d53f9-123">Monikers de pointeur</span><span class="sxs-lookup"><span data-stu-id="d53f9-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




