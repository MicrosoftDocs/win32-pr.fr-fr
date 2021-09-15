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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413684"
---
# <a name="error-handling-opengl"></a>Gestion des erreurs (OpenGL)

Lorsque OpenGL détecte une erreur, il enregistre un code d’erreur en cours. La fonction qui a provoqué l’erreur est ignorée et n’a donc aucun effet sur l’État OpenGL ou sur le contenu trame. (Si l’erreur enregistrée était GL \_ Mémoire insuffisante \_ \_ , toutefois, les résultats de la fonction ne sont pas définis.) Une fois enregistré, le code d’erreur actuel n’est pas effacé tant que vous n’avez pas appelé la fonction de requête [**glGetError**](glgeterror.md) , qui retourne le code d’erreur actuel.

Les implémentations de OpenGL peuvent retourner plusieurs codes d’erreur actuels, chacun restant défini jusqu’à la requête. La fonction **glGetError** retourne GL \_ no \_ Error une fois que vous avez interrogé tous les codes d’erreur actuels ou qu’il n’y a pas d’erreur. Par conséquent, si vous obtenez un code d’erreur, appelez **glGetError** jusqu’à ce qu' \_ aucune \_ erreur ne soit retournée pour vous assurer que vous avez détecté toutes les erreurs. Pour obtenir la liste des codes d’erreur, consultez [codes d’erreur OpenGL](opengl-error-codes.md).

Vous pouvez utiliser la fonction [**gluErrorString**](gluerrorstring.md) Glu pour obtenir une chaîne descriptive correspondant au code d’erreur transmis. Pour plus d’informations sur **gluErrorString**, consultez [gestion des erreurs](handling-errors.md).

> [!Note]  
> Les fonctions GLU retournent souvent des valeurs d’erreur si une erreur est détectée. En outre, la bibliothèque d’utilitaire OpenGL définit les codes d’erreur GLU \_ enum non valide \_ , Glu \_ valeur non valide \_ et Glu \_ de mémoire insuffisante \_ \_ , qui ont la même signification que les codes d’erreur OpenGL associés.

 

 

 




