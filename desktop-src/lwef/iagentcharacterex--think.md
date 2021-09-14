---
title: IAgentCharacterEx réfléchir
description: IAgentCharacterEx réfléchir
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221009"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx :: pensez

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Affiche la bulle de mot de pensée du caractère avec le texte spécifié.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texte à afficher dans la bulle d’idée du caractère.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande de **réflexion** .

</dd> </dl>

À l’instar de la méthode [**IAgentCharacter :: Speak**](iagentcharacter--speak.md) , la méthode de **réflexion** est une demande en file d’attente qui affiche du texte dans une bulle de mot, sauf que les pensées s’affichent dans une bulle d’idées spéciale. La bulle de réflexion ne prend en charge que la balise de contrôle de voix de signets (**\\ MRK**) et ignore toutes les autres balises de contrôle vocal. Contrairement à **IAgentCharacter :: Speak**, la méthode de **réflexion** ne modifie pas l’état d’animation du caractère.

Les paramètres de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) s’appliquent également au style d’apparence de la bulle de pensée. Par exemple, la propriété [**Enabled**](enabled-property.md) de la bulle doit également avoir la **valeur true** pour que le texte s’affiche.

La césure automatique des mots de Microsoft Agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace et tabulation). Toutefois, il peut également endommager un mot pour l’ajuster à l’info-bulle. Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un espace de largeur nulle (0x200B) Unicode entre les caractères pour définir des césures lexicales.

> [!Note]  
> Définissez l’ID de langue du caractère (à l’aide de [**IAgentCharacterEx :: SetLanguageID**](iagentcharacterex--setlanguageid.md) avant d’utiliser la méthode [**IAgentCharacter :: Speak**](iagentcharacter--speak.md) pour garantir l’affichage du texte approprié dans la bulle.

 

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon :: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx :: SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md)


 

 