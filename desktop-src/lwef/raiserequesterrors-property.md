---
title: Propriété RaiseRequestErrors
description: Propriété RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104199203"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="84e93-103">Propriété RaiseRequestErrors</span><span class="sxs-lookup"><span data-stu-id="84e93-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="84e93-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84e93-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="84e93-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="84e93-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="84e93-106">Retourne ou définit une valeur indiquant si les erreurs pour les demandes sont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="84e93-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="84e93-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="84e93-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="84e93-108">\*agent \* \* *. RaiseRequestErrors* \*  \[  =  *booléen*\]</span><span class="sxs-lookup"><span data-stu-id="84e93-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="84e93-109">Partie</span><span class="sxs-lookup"><span data-stu-id="84e93-109">Part</span></span>      | <span data-ttu-id="84e93-110">Description</span><span class="sxs-lookup"><span data-stu-id="84e93-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e93-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="84e93-111">*boolean*</span></span> | <span data-ttu-id="84e93-112">Valeur booléenne qui détermine si les erreurs dans les demandes sont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="84e93-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="84e93-113">**True**    (valeur par défaut) les erreurs de requête sont générées.</span><span class="sxs-lookup"><span data-stu-id="84e93-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="84e93-114">**Valeur false**     Les erreurs de demande ne sont pas déclenchées.</span><span class="sxs-lookup"><span data-stu-id="84e93-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84e93-115">Notes</span><span class="sxs-lookup"><span data-stu-id="84e93-115">Remarks</span></span>

<span data-ttu-id="84e93-116">Cette propriété vous permet de déterminer si le serveur génère des erreurs qui se produisent avec les méthodes qui prennent en charge les objets de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="84e93-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="84e93-117">Par exemple, si vous spécifiez un nom d’animation qui n’existe pas dans une méthode [**Play**](play-method.md), le serveur génère une erreur (en affichant le message d’erreur), sauf si vous affectez la valeur **false** à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="84e93-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="84e93-118">Il peut être utile pour les langages de programmation qui ne fournissent pas de récupération lorsqu’une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="84e93-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="84e93-119">Toutefois, soyez vigilant lorsque vous affectez à cette propriété la **valeur false**, car il peut être plus difficile de trouver des erreurs dans votre code.</span><span class="sxs-lookup"><span data-stu-id="84e93-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

