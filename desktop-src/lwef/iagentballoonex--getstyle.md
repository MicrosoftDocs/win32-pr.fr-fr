---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840410"
---
# <a name="iagentballoonexgetstyle"></a>IAgentBalloonEx::GetStyle

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

Récupère les paramètres de style de la bulle de texte du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*
</dt> <dd>

Paramètres de style pour le mot-bulle, qui peut être une combinaison de l’une des valeurs suivantes :



| Valeur                                                                           | Description                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| const-style de bulle **abrégé non signé** **\_ \_ BALLOONON = 0x00000001 ;**<br/> | La bulle est prise en charge pour la sortie.                        |
| const : style de bulle **abrégé non signé** **\_ \_ SIZETOTEXT = 0x0000002 ;**           | La hauteur de la bulle est dimensionnée pour s’adapter à la sortie de texte. |
| const-style de bulle **abrégé non signé** - **\_ \_ Masquer automatiquement = 0x00000004 ;**            | L’info-bulle est automatiquement masquée.                        |
| autorythme du style de la bulle **non signée const** **\_ \_ = 0x00000008 ;**            | La sortie de texte est basée sur la vitesse de sortie.          |



 

</dd> </dl>

Lorsque le bit de style **BalloonOn** est défini, la bulle de texte s’affiche lorsque la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace son affichage par le biais de la feuille de propriétés de l’agent Microsoft. Si la valeur n’est pas définie, aucune bulle ne s’affiche.

Lorsque le bit de style **SizeToText** est défini, le mot bulle redimensionne automatiquement la hauteur de la bulle sur la taille actuelle du texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) . Lorsque cette option n’est pas définie, la hauteur de l’info-bulle est basée sur le paramètre de propriété Number of Lines du ballon. Ce bit de style est défini sur 1 et toute tentative d’utilisation de [**IAgentBalloonEx :: SetNumLines**](iagentballoonex--setnumlines.md) génère une erreur.

Lorsque le bit de style de **masquage** automatique est défini, la bulle de mot se masque automatiquement après un court délai d’attente. Lorsqu’elle n’est pas définie, la bulle s’affiche jusqu’à un nouvel appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) , le caractère est masqué ou l’utilisateur clique ou fait glisser le caractère.

Lorsque le bit de style de **rythme** automatique est défini, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois. Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé. Si la valeur n’est pas définie, tout le texte inclus dans une instruction [**Speak**](speak-method.md) ou [**Song**](think-method.md) s’affiche à la fois.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

Les valeurs par défaut de ces bits de style sont basées sur les paramètres lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloonEx :: SetStyle**](iagentballoonex--setstyle.md)


 

 





