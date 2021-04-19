---
description: Les applications peuvent utiliser en toute sécurité les fonctionnalités de gestion de la mémoire de la bibliothèque Runtime C (malloc, Free, etc.) et C++ (New, Delete, etc.).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Fonctions de la bibliothèque C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524496"
---
# <a name="standard-c-library-functions"></a>Fonctions de la bibliothèque C standard

Les applications peuvent utiliser en toute sécurité les fonctionnalités de gestion de la mémoire de la bibliothèque Runtime C (**malloc**, **Free**, etc.) et C++ (**New**, **Delete**, etc.). Les fonctions de la bibliothèque Runtime C ne présentent pas les problèmes potentiels sous Windows 16 bits. La gestion de la mémoire n’est plus un problème, car le système est libre de gérer la mémoire en déplaçant les pages de la mémoire physique sans affecter les adresses virtuelles. De même, la distinction entre les pointeurs near et Far n’est plus pertinente. Par conséquent, vous pouvez utiliser les fonctions de la bibliothèque C standard pour la gestion de la mémoire. Toutefois, les fonctions de gestion de la mémoire fournissent des fonctionnalités qui ne sont pas disponibles dans la bibliothèque Runtime C.

 

 



