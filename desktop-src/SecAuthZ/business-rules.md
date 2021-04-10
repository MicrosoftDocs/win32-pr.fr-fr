---
description: Une règle d’entreprise permet à une application d’utiliser la logique au moment de l’exécution pour qualifier les autorisations accordées au client.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Règles d'entreprise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211078"
---
# <a name="business-rules"></a><span data-ttu-id="ab3ff-103">Règles d'entreprise</span><span class="sxs-lookup"><span data-stu-id="ab3ff-103">Business Rules</span></span>

<span data-ttu-id="ab3ff-104">Une règle d’entreprise permet à une application d’utiliser la logique au moment de l’exécution pour qualifier les autorisations accordées au client.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="ab3ff-105">Une règle d’entreprise est un script écrit dans le langage de programmation Visual Basic Scripting Edition (VBScript) ou écrit à l’aide du logiciel de développement Microsoft JScript qui est associé à un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="ab3ff-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="ab3ff-106">Lorsqu’une application vérifie l’accès pour une opération, le gestionnaire d’autorisations vérifie d’abord si le client actuel a accès à toutes les tâches qui contiennent cette opération, mais qui ne sont pas associées à des règles d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="ab3ff-107">Si l’accès n’est pas accordé de cette manière, le gestionnaire d’autorisations exécute des scripts de règle d’entreprise associés à toute tâche qui contient l’opération.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="ab3ff-108">Une application transmet des informations à un script de règle d’entreprise sous la forme d’une paire de tableaux représentant les noms et les valeurs des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="ab3ff-109">Le script a accès à ces paramètres par le biais d’un objet [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) qui est créé lors de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="ab3ff-110">Un script de règle d’entreprise ne peut pas être assigné à une tâche contenue dans une étendue déléguée.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab3ff-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab3ff-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab3ff-112">Accès éligible avec la logique métier en C++</span><span class="sxs-lookup"><span data-stu-id="ab3ff-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



