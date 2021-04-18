---
description: Les \_ constantes LINETSPIOPTION décrivent les fournisseurs de service de commande qui doivent être appelés.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533253"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="6bbb8-103">\_Constantes LINETSPIOPTION</span><span class="sxs-lookup"><span data-stu-id="6bbb8-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="6bbb8-104">Les **\_ constantes LINETSPIOPTION** décrivent les fournisseurs de service de commande qui doivent être appelés.</span><span class="sxs-lookup"><span data-stu-id="6bbb8-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="6bbb8-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**</span><span class="sxs-lookup"><span data-stu-id="6bbb8-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6bbb8-106">L’interface TAPI doit appeler les fonctions de ce fournisseur de services une à la fois ; il doit attendre que chaque fonction retourne (mais pas pour que les fonctions asynchrones se terminent) avant d’appeler la même fonction ou une autre fonction, sur le même thread ou sur un autre, sur le même processeur ou sur un processeur différent.</span><span class="sxs-lookup"><span data-stu-id="6bbb8-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bbb8-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bbb8-107">Requirements</span></span>



| <span data-ttu-id="6bbb8-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bbb8-108">Requirement</span></span> | <span data-ttu-id="6bbb8-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bbb8-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6bbb8-110">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6bbb8-110">TAPI version</span></span><br/> | <span data-ttu-id="6bbb8-111">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6bbb8-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6bbb8-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bbb8-112">Header</span></span><br/>       | <dl> <span data-ttu-id="6bbb8-113"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bbb8-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




