---
description: Cette vue d’ensemble présente les propriétés de la fenêtre.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: À propos des propriétés de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202919"
---
# <a name="about-window-properties"></a>À propos des propriétés de fenêtre

Une *propriété de fenêtre* correspond à toutes les données affectées à une fenêtre. Une propriété de fenêtre est généralement un handle des données spécifiques à la fenêtre, mais il peut s’agir de n’importe quelle valeur. Chaque propriété de fenêtre est identifiée par un nom de chaîne. Plusieurs fonctions permettent aux applications d’utiliser les propriétés de la fenêtre. Cette vue d’ensemble aborde les sujets suivants :

-   [Avantages de l’utilisation des propriétés de la fenêtre](#advantages-of-using-window-properties)
-   [Affecter des propriétés de fenêtre](#assigning-window-properties)
-   [Énumération des propriétés de la fenêtre](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Avantages de l’utilisation des propriétés de la fenêtre

Les propriétés de fenêtre sont généralement utilisées pour associer des données à une fenêtre sous-classée ou à une fenêtre dans une application d’interface multidocument (MDI). Dans les deux cas, il n’est pas pratique d’utiliser les octets supplémentaires spécifiés dans la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou la structure de classe pour les deux raisons suivantes :

-   Une application peut ne pas connaître le nombre d’octets supplémentaires disponibles ou la manière dont l’espace est utilisé. En utilisant les propriétés de la fenêtre, l’application peut associer des données à une fenêtre sans accéder aux octets supplémentaires.
-   Une application doit accéder aux octets supplémentaires à l’aide de décalages. Toutefois, les propriétés de la fenêtre sont accessibles par leurs identificateurs de chaîne, et non par des décalages.

Pour plus d’informations sur le sous-classement, consultez [sous-classe de procédure de fenêtre](about-window-procedures.md). Pour plus d’informations sur les fenêtres MDI, consultez [interface multidocument](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Affecter des propriétés de fenêtre

La fonction [**échec SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) assigne une propriété de fenêtre et son identificateur de chaîne à une fenêtre. La fonction [**getprop**](/windows/win32/api/winuser/nf-winuser-getpropa) récupère la propriété de fenêtre identifiée par la chaîne spécifiée. La fonction [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) détruit l’association entre une fenêtre et une propriété de fenêtre, mais ne détruit pas les données elles-mêmes. Pour supprimer les données elles-mêmes, utilisez la fonction appropriée pour libérer le handle retourné par **RemoveProp**.

## <a name="enumerating-window-properties"></a>Énumération des propriétés de la fenêtre

Les fonctions [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) et [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) énumèrent toutes les propriétés d’une fenêtre à l’aide d’une fonction de rappel définie par l’application. Pour plus d’informations sur la fonction de rappel, consultez [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) comprend un paramètre supplémentaire pour les données définies par l’application utilisées par la fonction de rappel. Pour plus d’informations sur la fonction de rappel, consultez [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
