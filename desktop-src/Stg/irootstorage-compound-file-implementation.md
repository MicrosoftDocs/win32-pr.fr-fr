---
title: IRootStorage-implémentation de fichier composé
description: L’implémentation de fichier composé de COM de IRootStorage vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible. Pour plus d’informations sur le comportement de cette interface, consultez IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675913"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="49f12-105">IRootStorage-implémentation de fichier composé</span><span class="sxs-lookup"><span data-stu-id="49f12-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="49f12-106">L’implémentation de fichier composé de COM de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible.</span><span class="sxs-lookup"><span data-stu-id="49f12-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="49f12-107">Pour plus d’informations sur le comportement de cette interface, consultez **IRootStorage**.</span><span class="sxs-lookup"><span data-stu-id="49f12-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="49f12-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="49f12-108">When to Use</span></span>

<span data-ttu-id="49f12-109">Utilisez l’implémentation fournie par le système de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) uniquement pour prendre en charge l’enregistrement de fichiers dans des conditions de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="49f12-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="49f12-110">Notes</span><span class="sxs-lookup"><span data-stu-id="49f12-110">Remarks</span></span>

<span data-ttu-id="49f12-111">Il est possible d’appeler l’implémentation COM de [**IRootStorage :: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) pour effectuer une opération Enregistrer sous normale dans un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="49f12-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="49f12-112">Toutefois, les applications qui le font peuvent ne pas être compatibles avec les futures générations de stockage COM.</span><span class="sxs-lookup"><span data-stu-id="49f12-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="49f12-113">Pour éviter cette éventualité, les applications effectuant une opération Enregistrer sous doivent créer manuellement le deuxième fichier composé et appeler [**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span><span class="sxs-lookup"><span data-stu-id="49f12-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="49f12-114">La méthode **IRootStorage :: SwitchToFile** doit être utilisée uniquement dans les situations d’urgence (mémoire insuffisante ou espace disque).</span><span class="sxs-lookup"><span data-stu-id="49f12-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f12-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49f12-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f12-116">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="49f12-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="49f12-117">**IRootStorage::SwitchToFile**</span><span class="sxs-lookup"><span data-stu-id="49f12-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




