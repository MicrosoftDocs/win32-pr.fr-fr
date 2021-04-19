---
description: Une fonction d’installation peut afficher une boîte de dialogue de message d’erreur qui retourne l’une des erreurs suivantes. Une boîte d’erreur s’affiche uniquement si le niveau de l’interface utilisateur est complet, réduit ou de base. Pour plus d’informations, consultez niveaux de l’interface utilisateur.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Messages d’erreur affichés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544755"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="06013-105">Messages d’erreur affichés</span><span class="sxs-lookup"><span data-stu-id="06013-105">Displayed Error Messages</span></span>

<span data-ttu-id="06013-106">Une [fonction d’installation](installer-function-reference.md) peut afficher une boîte de dialogue de message d’erreur qui retourne l’une des erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="06013-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="06013-107">Une boîte d’erreur s’affiche uniquement si le niveau de l’interface utilisateur est complet, réduit ou de base.</span><span class="sxs-lookup"><span data-stu-id="06013-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="06013-108">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="06013-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="06013-109">Les fonctions du programme d’installation affichent uniquement les messages d’erreur répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="06013-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="06013-110">Pour les erreurs qui ne sont pas dans cette liste, l’appelant de la fonction est responsable de la gestion de l’affichage des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="06013-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="06013-111">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="06013-111">Error code</span></span>               | <span data-ttu-id="06013-112">Error</span><span class="sxs-lookup"><span data-stu-id="06013-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="06013-113">ERREUR d' \_ installation d' \_ interruption</span><span class="sxs-lookup"><span data-stu-id="06013-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="06013-114">L’installation a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="06013-114">The install was suspended.</span></span>   |
| <span data-ttu-id="06013-115">ERREUR lors de l' \_ installation de \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="06013-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="06013-116">L’utilisateur a quitté l’installation.</span><span class="sxs-lookup"><span data-stu-id="06013-116">The user exited the install.</span></span> |
| <span data-ttu-id="06013-117">ERREUR d' \_ installation \_</span><span class="sxs-lookup"><span data-stu-id="06013-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="06013-118">Échec de l’installation.</span><span class="sxs-lookup"><span data-stu-id="06013-118">Install failed.</span></span>              |



 

 

 



