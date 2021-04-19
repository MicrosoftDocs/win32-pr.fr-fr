---
description: Si l’option de traitement de retour msidbCustomActionTypeContinue n’est pas définie, l’action personnalisée doit retourner un code d’État entier comme indiqué dans le tableau suivant.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valeurs de retour de l’action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530918"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="8cfac-103">Valeurs de retour de l’action personnalisée</span><span class="sxs-lookup"><span data-stu-id="8cfac-103">Custom Action Return Values</span></span>

<span data-ttu-id="8cfac-104">Si l’option de traitement de retour **msidbCustomActionTypeContinue** n’est pas définie, l’action personnalisée doit retourner un code d’État entier comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8cfac-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="8cfac-105">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cfac-105">Return value</span></span>                 | <span data-ttu-id="8cfac-106">Description</span><span class="sxs-lookup"><span data-stu-id="8cfac-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="8cfac-107">fonction d’erreur \_ \_ non \_ appelée</span><span class="sxs-lookup"><span data-stu-id="8cfac-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="8cfac-108">Action non exécutée.</span><span class="sxs-lookup"><span data-stu-id="8cfac-108">Action not executed.</span></span>                  |
| <span data-ttu-id="8cfac-109">ERREUR de \_ réussite</span><span class="sxs-lookup"><span data-stu-id="8cfac-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="8cfac-110">Actions terminées avec succès.</span><span class="sxs-lookup"><span data-stu-id="8cfac-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="8cfac-111">ERREUR lors de l' \_ installation de \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="8cfac-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="8cfac-112">L’utilisateur s’est arrêté prématurément.</span><span class="sxs-lookup"><span data-stu-id="8cfac-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="8cfac-113">ERREUR d' \_ installation \_</span><span class="sxs-lookup"><span data-stu-id="8cfac-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="8cfac-114">Une erreur irrécupérable s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8cfac-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="8cfac-115">ERREUR \_ aucun \_ autre \_ élément</span><span class="sxs-lookup"><span data-stu-id="8cfac-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="8cfac-116">Ignorer les actions restantes, et non pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="8cfac-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="8cfac-117">Notez que les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="8cfac-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="8cfac-118">Le programme d’installation interprète toute autre valeur de retour comme un échec.</span><span class="sxs-lookup"><span data-stu-id="8cfac-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="8cfac-119">Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="8cfac-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="8cfac-120">Pour plus d’informations sur l’option **msidbCustomActionTypeContinue** et d’autres options de traitement des retours, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="8cfac-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="8cfac-121">Notez que Windows Installer traduit les valeurs de retour de toutes les actions lorsqu’il écrit la valeur de retour dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="8cfac-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="8cfac-122">Par exemple, si la valeur de retour de l’action apparaît comme 1 dans le fichier journal, cela signifie que l’action a retourné une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="8cfac-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="8cfac-123">Pour plus d’informations sur cette traduction, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8cfac-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cfac-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8cfac-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cfac-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8cfac-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="8cfac-126">Journalisation des valeurs de retour d’action</span><span class="sxs-lookup"><span data-stu-id="8cfac-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



