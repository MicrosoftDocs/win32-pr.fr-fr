---
description: Vous ne pouvez pas créer d’instances des classes modifiées dans l’espace de noms localisé. Les classes modifiées dans l’espace de noms localisé sont traitées comme si elles étaient abstraites, bien qu’elles ne contiennent pas de qualificateur abstrait.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considérations relatives aux classes modifiées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211064"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="cdbfe-104">Considérations relatives aux classes modifiées</span><span class="sxs-lookup"><span data-stu-id="cdbfe-104">Amended Class Considerations</span></span>

<span data-ttu-id="cdbfe-105">Vous ne pouvez pas créer d’instances des classes modifiées dans l’espace de noms localisé.</span><span class="sxs-lookup"><span data-stu-id="cdbfe-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="cdbfe-106">Les classes modifiées dans l’espace de noms localisé sont traitées comme si elles étaient abstraites, bien qu’elles ne contiennent pas de qualificateur [**abstrait**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="cdbfe-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="cdbfe-107">Si vous récupérez une classe modifiée à partir d’un espace de noms localisé à l’aide de l’indicateur WBEM \_ \_ utiliser des \_ \_ qualificateurs modifiés et générer une instance à partir de celle-ci, l’instance contient tous les qualificateurs modifiés de la classe modifiée.</span><span class="sxs-lookup"><span data-stu-id="cdbfe-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="cdbfe-108">Vous ne pouvez pas stocker cette nouvelle classe dans l’espace de noms qui contient la définition de classe de base, sauf si vous effectuez l’opération **put** avec l’indicateur WBEM \_ utiliser des \_ \_ \_ qualificateurs modifiés.</span><span class="sxs-lookup"><span data-stu-id="cdbfe-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="cdbfe-109">Cet indicateur demande à WMI de supprimer tous les qualificateurs modifiés avant d’enregistrer l’objet.</span><span class="sxs-lookup"><span data-stu-id="cdbfe-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="cdbfe-110">Si vous ne spécifiez pas \_ d’indicateur WBEM \_ utiliser des \_ \_ qualificateurs modifiés, l’opération **put** échoue avec une erreur d’objet de \_ modification WBEM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cdbfe-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



