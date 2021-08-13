---
description: Un assembly Win32 peut être installé en tant qu’assembly privé et être disponible exclusivement pour une utilisation par une seule application. les assemblys privés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assemblys privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cc9bd9c9f4c5230dcb24ed7059f6817d4c5f3c7cfdeb4b7cfd25d95ca2a3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327842"
---
# <a name="private-assemblies"></a>Assemblys privés

Un assembly Win32 peut être installé en tant qu’assembly privé et être disponible exclusivement pour une utilisation par une seule application. les assemblys privés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.

sur Windows XP, les assemblys privés sont installés en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). le Windows Installer installe des assemblys côte à côte privés dans un dossier privé pour l’application. Généralement le dossier qui contient le fichier exécutable de l’application. La dépendance de l’application sur l’assembly privé est spécifiée dans un fichier manifeste de l’application. Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

sur les systèmes d’exploitation antérieurs à Windows XP, une copie de l’assembly privé et d’un fichier. local est installée dans un dossier privé pour l’utilisation exclusive de l’application. Une version de l’assembly est également inscrite globalement sur le système et disponible pour toutes les applications qui y sont liées. La version globale de l’assembly peut être la version installée avec l’application ou une version antérieure. La version globale est déterminée par les mêmes règles que celles utilisées par les [composants isolés](isolated-components.md).

notez que le Windows Installer ne peut pas installer un assembly privé dans un emplacement dont le chemin d’accès contient plus de 234 caractères, y compris le caractère null de fin.

 

 
