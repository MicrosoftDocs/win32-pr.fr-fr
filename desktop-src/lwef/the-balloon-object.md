---
title: Objet Balloon
description: Objet Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745971"
---
# <a name="the-balloon-object"></a>Objet Balloon

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Microsoft agent prend en charge le sous-titrage textuel de la méthode [**Speak**](speak-method.md) à l’aide d’une bulle de texte animé. La méthode de [**réflexion**](think-method.md) vous permet d’afficher du texte sans sortie audio dans une bulle de mot « pensée ».

Les valeurs par défaut de la fenêtre de la bulle initiale d’un caractère sont définies et compilées dans l’éditeur de caractères Microsoft Agent. Une fois exécuté, les propriétés [**activées**](enabled-property.md) et de [**police**](https://www.bing.com/search?q=**Font**) de l’info-bulle peuvent être remplacées par l’utilisateur. Si un utilisateur modifie les propriétés de la bulle de mot, il affecte tous les caractères. Les bulles de mot [**parole**](speak-method.md) et de [**réflexion**](think-method.md) utilisent les mêmes paramètres de propriété pour la taille. Vous pouvez accéder aux propriétés de la bulle de texte d’un caractère par le biais de l’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) , qui est un enfant de l’objet [**character**](/windows/desktop/lwef/the-characters-object) .

L’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) prend en charge les propriétés suivantes :

-   [**BackColor**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**Activé**](enabled-property.md)
-   [**FontCharSet**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**Gras**](fontbold-property.md)
-   [**Italique**](fontitalic-property.md)
-   [**FontSize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**Souligné**](fontunderline-property.md)
-   [**CouleurTexte**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Style**](style-property.md)
-   [**Parent**](visible-property-bal.md)

 

 