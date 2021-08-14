---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3961bf5f32aad10c662d9dc2943f32b60fad485621b5adce32e2036e6d2d4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478539"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx :: SetStyle

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Récupère les paramètres de style de la bulle de texte du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

Paramètres de style pour le mot-bulle, qui peut être une combinaison de l’une des valeurs suivantes :



| Valeur                                                                            | Description                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| const-style de bulle **abrégé non signé** **\_ \_ BALLOONON = 0x00000001 ;**<br/>  | La bulle est prise en charge pour la sortie.                        |
| const : style de bulle **abrégé non signé** **\_ \_ SIZETOTEXT = 0x0000002 ;**<br/> | La hauteur de la bulle est dimensionnée pour s’adapter à la sortie de texte. |
| const-style de bulle **abrégé non signé** - **\_ \_ Masquer automatiquement = 0x00000004 ;**<br/>  | L’info-bulle est automatiquement masquée.                        |
| autorythme du style de la bulle **non signée const** **\_ \_ = 0x00000008 ;**<br/>  | La sortie de texte est basée sur la vitesse de sortie.          |



 

</dd> </dl>

Lorsque le bit de style **BalloonOn** est défini, la bulle de mot apparaît lorsque la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) est utilisée, sauf si l’utilisateur remplace son affichage dans la feuille de propriétés de l’agent Microsoft. Si la valeur n’est pas définie, aucune bulle ne s’affiche.

Lorsque le bit de style **SizeToText** est défini, le mot bulle redimensionne automatiquement la hauteur de la bulle sur la taille actuelle du texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) . Lorsque cette option n’est pas définie, la hauteur de l’info-bulle est basée sur le paramètre de propriété Number of Lines du ballon. Ce bit de style est défini sur 1 et toute tentative d’utilisation de [**IAgentBalloonEx :: SetNumLines**](iagentballoonex--setnumlines.md) génère une erreur.

Lorsque le bit de style de **masquage** automatique est défini, la bulle de mot est automatiquement masquée après un délai d’expiration courts. Lorsqu’elle n’est pas définie, la bulle s’affiche jusqu’à un nouvel appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) , le caractère est masqué ou l’utilisateur clique ou fait glisser le caractère.

Lorsque le bit de style de **rythme** automatique est défini, la bulle de mot ajuste la sortie en fonction du taux de sortie actuel, par exemple, un mot à la fois. Lorsque la sortie dépasse la taille de la bulle, le texte précédent est automatiquement défilé. Si la valeur n’est pas définie, tout le texte inclus dans une instruction [**Speak**](speak-method.md) ou [**Song**](think-method.md) s’affiche à la fois.

La propriété style de l’info-bulle peut être définie même si l’utilisateur a désactivé l’affichage de l’info-bulle à l’aide de la feuille de propriétés Microsoft Agent.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

Les valeurs par défaut de ces bits de style sont basées sur leurs paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md)


 

 





