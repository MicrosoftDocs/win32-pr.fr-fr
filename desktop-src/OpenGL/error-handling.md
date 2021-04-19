---
title: Gestion des erreurs (OpenGL)
description: Lorsque OpenGL détecte une erreur, il enregistre un code d’erreur en cours.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- gestion des erreurs OpenGL
- Gestion des erreurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511338"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="598af-105">Gestion des erreurs (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="598af-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="598af-106">Lorsque OpenGL détecte une erreur, il enregistre un code d’erreur en cours.</span><span class="sxs-lookup"><span data-stu-id="598af-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="598af-107">La fonction qui a provoqué l’erreur est ignorée et n’a donc aucun effet sur l’État OpenGL ou sur le contenu trame.</span><span class="sxs-lookup"><span data-stu-id="598af-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="598af-108">(Si l’erreur enregistrée était GL \_ Mémoire insuffisante \_ \_ , toutefois, les résultats de la fonction ne sont pas définis.) Une fois enregistré, le code d’erreur actuel n’est pas effacé tant que vous n’avez pas appelé la fonction de requête [**glGetError**](glgeterror.md) , qui retourne le code d’erreur actuel.</span><span class="sxs-lookup"><span data-stu-id="598af-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="598af-109">Les implémentations de OpenGL peuvent retourner plusieurs codes d’erreur actuels, chacun restant défini jusqu’à la requête.</span><span class="sxs-lookup"><span data-stu-id="598af-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="598af-110">La fonction **glGetError** retourne GL \_ no \_ Error une fois que vous avez interrogé tous les codes d’erreur actuels ou qu’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="598af-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="598af-111">Par conséquent, si vous obtenez un code d’erreur, appelez **glGetError** jusqu’à ce qu' \_ aucune \_ erreur ne soit retournée pour vous assurer que vous avez détecté toutes les erreurs.</span><span class="sxs-lookup"><span data-stu-id="598af-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="598af-112">Pour obtenir la liste des codes d’erreur, consultez [codes d’erreur OpenGL](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="598af-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="598af-113">Vous pouvez utiliser la fonction [**gluErrorString**](gluerrorstring.md) Glu pour obtenir une chaîne descriptive correspondant au code d’erreur transmis.</span><span class="sxs-lookup"><span data-stu-id="598af-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="598af-114">Pour plus d’informations sur **gluErrorString**, consultez [gestion des erreurs](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="598af-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="598af-115">Les fonctions GLU retournent souvent des valeurs d’erreur si une erreur est détectée.</span><span class="sxs-lookup"><span data-stu-id="598af-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="598af-116">En outre, la bibliothèque d’utilitaire OpenGL définit les codes d’erreur GLU \_ enum non valide \_ , Glu \_ valeur non valide \_ et Glu \_ de mémoire insuffisante \_ \_ , qui ont la même signification que les codes d’erreur OpenGL associés.</span><span class="sxs-lookup"><span data-stu-id="598af-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




