---
description: ICE89 vérifie que la valeur de la \_ colonne parent ProgID dans la table ProgID est une clé étrangère valide dans la colonne ProgID de la table ProgID. Chaque parent ProgId doit avoir un enregistrement dans la table ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952729"
---
# <a name="ice89"></a><span data-ttu-id="93644-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="93644-104">ICE89</span></span>

<span data-ttu-id="93644-105">ICE89 vérifie que la valeur de la \_ colonne parent ProgID dans la [table ProgID](progid-table.md) est une clé étrangère valide dans la colonne ProgID de la table ProgID.</span><span class="sxs-lookup"><span data-stu-id="93644-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="93644-106">Chaque parent ProgId doit avoir un enregistrement dans la table ProgId.</span><span class="sxs-lookup"><span data-stu-id="93644-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="93644-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="93644-107">Result</span></span>

<span data-ttu-id="93644-108">ICE89 publie les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93644-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="93644-109">Erreur ICE89</span><span class="sxs-lookup"><span data-stu-id="93644-109">ICE89 error</span></span>                                                           | <span data-ttu-id="93644-110">Description</span><span class="sxs-lookup"><span data-stu-id="93644-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="93644-111">Le \_ parent ProgID « \[ 1 \] » dans la table ProgID n’est pas un ProgID valide.</span><span class="sxs-lookup"><span data-stu-id="93644-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="93644-112">Un parent ProgId spécifié n’est pas listé dans la table ProgId.</span><span class="sxs-lookup"><span data-stu-id="93644-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93644-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93644-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93644-114">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="93644-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



