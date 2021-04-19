---
description: Un lien symbolique est un objet de système de fichiers qui pointe vers un autre objet de système de fichiers. L’objet désigné est appelé la cible.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Liens symboliques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545045"
---
# <a name="symbolic-links"></a>Liens symboliques

Un lien symbolique est un objet de système de fichiers qui pointe vers un autre objet de système de fichiers. L’objet désigné est appelé la cible.

Les liens symboliques sont transparents pour les utilisateurs ; les liens apparaissent en tant que fichiers ou répertoires normaux et peuvent être traités par l’utilisateur ou l’application exactement de la même manière.

Les liens symboliques sont conçus pour faciliter la migration et la compatibilité des applications avec les systèmes d’exploitation UNIX. Microsoft a implémenté ses liens symboliques pour fonctionner comme des liens UNIX.

Pour plus d'informations, consultez les rubriques ci-dessous.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                             | Description                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Effets de liens symboliques sur les fonctions des systèmes de fichiers](symbolic-link-effects-on-file-systems-functions.md)<br/> | La façon dont les liens symboliques affectent les fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers.<br/>                                        |
| [Considérations relatives à la programmation](symbolic-link-programming-considerations.md)<br/>                             | Considérations relatives à la programmation pour l’utilisation des liens symboliques.<br/>                                                                                |
| [Création de liens symboliques](creating-symbolic-links.md)<br/>                                                 | Créez des liens symboliques qui utilisent un chemin d’accès absolu ou relatif à l’aide de la fonction [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .<br/> |



 

## <a name="supported-operating-systems"></a>Systèmes d’exploitation pris en charge

Les liens symboliques sont disponibles dans NTFS à partir de Windows Vista.

 

 




