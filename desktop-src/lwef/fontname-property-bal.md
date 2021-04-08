---
title: Propriété FontName (objet Balloon)
description: FontName, propriété
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102733"
---
# <a name="fontname-property-balloon-object"></a>Propriété FontName (objet Balloon)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la police utilisée dans le mot-bulle pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Police Balloon. FontName_ *  \[  =  \]



| Partie   | Description                                      |
|--------|--------------------------------------------------|
| *son* | Valeur de chaîne correspondant au nom de la police. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété [**FontName**](fontname-property.md) définit la police utilisée pour afficher le texte de la fenêtre de la bulle de texte d’une chaîne. La valeur par défaut des paramètres de police de la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent. En outre, l’utilisateur peut remplacer les paramètres de police pour tous les caractères de la feuille de propriétés de l’agent Microsoft.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> Si vous utilisez un caractère que vous n’avez pas compilé, vérifiez les propriétés [**FontName**](fontname-property.md) et [**FontCharSet**](fontcharset-property.md) pour déterminer s’ils sont appropriés pour vos paramètres régionaux. Vous devrez peut-être définir ces valeurs avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.

 

 

 




