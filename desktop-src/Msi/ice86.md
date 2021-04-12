---
description: ICE86 émet un avertissement si le package utilise la propriété AdminUser dans la colonne de base de données du type de condition. Les auteurs de package doivent utiliser la propriété Privileged dans les instructions conditionnelles.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320085"
---
# <a name="ice86"></a><span data-ttu-id="b4e81-104">ICE86</span><span class="sxs-lookup"><span data-stu-id="b4e81-104">ICE86</span></span>

<span data-ttu-id="b4e81-105">ICE86 émet un avertissement si le package utilise la propriété [**adminuser**](adminuser.md) dans la colonne de base de données du type de [condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e81-105">ICE86 issues a warning if the package uses the [**AdminUser**](adminuser.md) property in database column of the [Condition](condition.md) type.</span></span> <span data-ttu-id="b4e81-106">Les auteurs de package doivent utiliser la propriété [**Privileged**](privileged.md) dans les instructions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="b4e81-106">Package authors should use the [**Privileged**](privileged.md) property in conditional statements.</span></span>

## <a name="result"></a><span data-ttu-id="b4e81-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="b4e81-107">Result</span></span>

<span data-ttu-id="b4e81-108">ICE86 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="b4e81-108">ICE86 posts the following warning.</span></span>



| <span data-ttu-id="b4e81-109">AVERTISSEMENT ICE86</span><span class="sxs-lookup"><span data-stu-id="b4e81-109">ICE86 warning</span></span>                                                                                               | <span data-ttu-id="b4e81-110">Description</span><span class="sxs-lookup"><span data-stu-id="b4e81-110">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b4e81-111">Propriété \` % s \` trouvée dans la colonne \` % s \` . \` % s \` dans la ligne% s.</span><span class="sxs-lookup"><span data-stu-id="b4e81-111">Property \`%s\` found in column \`%s\`.\`%s\` in row %s.</span></span> <span data-ttu-id="b4e81-112">\`La \` propriété Privileged est souvent plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="b4e81-112">\`Privileged\` property is often more appropriate.</span></span> | <span data-ttu-id="b4e81-113">La propriété [**adminuser**](adminuser.md) a été utilisée dans un champ condition.</span><span class="sxs-lookup"><span data-stu-id="b4e81-113">[**AdminUser**](adminuser.md) property was used in a Condition field.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b4e81-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4e81-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4e81-115">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="b4e81-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



