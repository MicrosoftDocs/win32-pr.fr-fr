---
description: Cette section traite des propriétés de la fenêtre. Une propriété de fenêtre correspond à toutes les données affectées à une fenêtre.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Propriétés de la fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a06be9fca67dedeb98afd7a56638622dabc858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523081"
---
# <a name="window-properties"></a>Propriétés de la fenêtre

Une propriété de fenêtre correspond à toutes les données affectées à une fenêtre. Une propriété de fenêtre est généralement un handle des données spécifiques à la fenêtre, mais il peut s’agir de n’importe quelle valeur. Chaque propriété de fenêtre est identifiée par un nom de chaîne.

### <a name="in-this-section"></a>Dans cette section



| Nom                                                       | Description                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [À propos des propriétés de fenêtre](about-window-properties.md)     | Décrit les propriétés de la fenêtre.<br/>                                                   |
| [Utilisation des propriétés de la fenêtre](using-window-properties.md)     | Explique comment effectuer les tâches suivantes associées aux propriétés de la fenêtre.<br/> |
| [Référence des propriétés de la fenêtre](window-property-reference.md) | Contient la référence de l’API.<br/>                                                    |



 

### <a name="window-property-functions"></a>Fonctions de propriété de fenêtre



| Nom                                   | Description                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Énumère toutes les entrées de la liste de propriétés d’une fenêtre en les passant, un par un, à la fonction de rappel spécifiée. [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) se poursuit jusqu’à ce que la dernière entrée soit énumérée ou que la fonction de rappel retourne **false**.<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Énumère toutes les entrées de la liste de propriétés d’une fenêtre en les passant, un par un, à la fonction de rappel spécifiée. [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) se poursuit jusqu’à ce que la dernière entrée soit énumérée ou que la fonction de rappel retourne **false**. <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Récupère un handle de données de la liste de propriétés de la fenêtre spécifiée. La chaîne de caractères identifie le handle à récupérer. La chaîne et le descripteur doivent avoir été ajoutés à la liste de propriétés par un appel précédent à la fonction [**échec SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) . <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Fonction de rappel définie par l’application utilisée avec la fonction [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) . La fonction reçoit des entrées de propriété à partir de la liste de propriétés d’une fenêtre. Le type **PROPENUMPROC** définit un pointeur vers cette fonction de rappel. [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca) est un espace réservé pour le nom de la fonction définie par l’application. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Fonction de rappel définie par l’application utilisée avec la fonction [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) . La fonction reçoit des entrées de propriété à partir de la liste de propriétés d’une fenêtre. Le type **PROPENUMPROCEX** définit un pointeur vers cette fonction de rappel. [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) est un espace réservé pour le nom de la fonction définie par l’application. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Supprime une entrée de la liste de propriétés de la fenêtre spécifiée. La chaîne de caractères spécifiée identifie l’entrée à supprimer.<br/>                                                                                                                                                                                                                    |
| [**Échec SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Ajoute une nouvelle entrée ou modifie une entrée existante dans la liste de propriétés de la fenêtre spécifiée. La fonction ajoute une nouvelle entrée à la liste si la chaîne de caractères spécifiée n’existe pas déjà dans la liste. La nouvelle entrée contient la chaîne et le descripteur. Sinon, la fonction remplace le handle actuel de la chaîne par le handle spécifié. <br/> |



 

 

 
