---
title: Gestion des erreurs (OpenGL)
description: La fonction gluErrorString récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilitaire OpenGL (GLU), codes d’erreur
- GLU (utilitaire OpenGL), codes d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316985"
---
# <a name="handling-errors-opengl"></a><span data-ttu-id="f00f5-105">Gestion des erreurs (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="f00f5-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="f00f5-106">La fonction **gluErrorString** récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou Glu.</span><span class="sxs-lookup"><span data-stu-id="f00f5-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="f00f5-107">Les codes d’erreur OpenGL actuellement définis sont décrits dans [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="f00f5-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="f00f5-108">Les codes d’erreur GLU sont répertoriés dans [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)et [*gluNurbsCallback*](glunurbs.md).</span><span class="sxs-lookup"><span data-stu-id="f00f5-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="f00f5-109">La valeur de retour pour **gluErrorString** est un pointeur vers une chaîne descriptive qui correspond au numéro d’erreur OpenGL, Glu ou glx passé dans le paramètre *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="f00f5-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="f00f5-110">Les codes d’erreur définis sont décrits dans le *Manuel de référence OpenGL* avec la fonction ou la fonction qui peut les générer.</span><span class="sxs-lookup"><span data-stu-id="f00f5-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




