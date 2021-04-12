---
description: La fonction d’exportation ParserAutoInstallInfo identifie l’analyseur, ou les analyseurs qui se trouvent dans une DLL. ParserAutoInstallInfo doit être implémenté dans toutes les dll de l’analyseur.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Fonction de rappel ParserAutoInstallInfo (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318073"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="f7c37-104">ParserAutoInstallInfo fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="f7c37-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="f7c37-105">La fonction d’exportation **ParserAutoInstallInfo** identifie l’analyseur, ou les analyseurs qui se trouvent dans une dll.</span><span class="sxs-lookup"><span data-stu-id="f7c37-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="f7c37-106">**ParserAutoInstallInfo** doit être implémenté dans toutes les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c37-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7c37-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="f7c37-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7c37-108">Parameters</span></span>

<span data-ttu-id="f7c37-109">Cette fonction de rappel n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f7c37-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7c37-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7c37-110">Return value</span></span>

<span data-ttu-id="f7c37-111">Si la fonction réussit, la valeur de retour est une structure [ \_ PARSERDLLINFO de PF](pf-parserdllinfo.md) qui décrit les analyseurs dans la dll.</span><span class="sxs-lookup"><span data-stu-id="f7c37-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="f7c37-112">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="f7c37-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c37-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f7c37-113">Remarks</span></span>

<span data-ttu-id="f7c37-114">Lorsque Moniteur réseau se charge pour la première fois, il appelle **ParserAutoInstallInfo** (s’il existe) pour installer automatiquement chaque analyseur, puis énumère toutes les dll de l’analyseur dans le sous-répertoire de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="f7c37-115">Les informations retournées dans la structure **\_ PARSERDLLINFO de PF** incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f7c37-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="f7c37-116">Nombre d’analyseurs dans la DLL (en général, un).</span><span class="sxs-lookup"><span data-stu-id="f7c37-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="f7c37-117">Le nom et une brève description du protocole détecté par chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="f7c37-118">Fichier d’aide facultatif pour chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="f7c37-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="f7c37-119">Les protocoles qui précèdent chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="f7c37-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="f7c37-120">Les protocoles qui suivent chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="f7c37-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="f7c37-121">Chaque DLL de l’analyseur doit contenir un analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="f7c37-122">Toutefois, Moniteur réseau vous permet de créer une DLL qui contient plus d’un analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="f7c37-123">Par exemple, tcpip.dll est une Moniteur réseau DLL avec plus d’un analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="f7c37-124">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="f7c37-124">For information on</span></span>                                               | <span data-ttu-id="f7c37-125">Consultez</span><span class="sxs-lookup"><span data-stu-id="f7c37-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f7c37-126">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f7c37-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="f7c37-127">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="f7c37-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="f7c37-128">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="f7c37-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="f7c37-129">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="f7c37-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="f7c37-130">L’implémentation de **ParserAutoInstallInfo**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="f7c37-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="f7c37-131">Implémentation de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="f7c37-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="f7c37-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7c37-132">Requirements</span></span>



| <span data-ttu-id="f7c37-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7c37-133">Requirement</span></span> | <span data-ttu-id="f7c37-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7c37-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c37-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c37-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c37-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7c37-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f7c37-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c37-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c37-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7c37-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f7c37-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7c37-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7c37-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7c37-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7c37-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7c37-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c37-142">\_PARSERDLLINFO PF</span><span class="sxs-lookup"><span data-stu-id="f7c37-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




