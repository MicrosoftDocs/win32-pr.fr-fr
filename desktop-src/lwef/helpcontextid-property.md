---
title: HelpContextID, propriété (objet collection Commands)
description: En savoir plus sur la propriété HelpContextID de l’objet de collection Commands. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0635f62350d0bea31afda09b04e6489fe7f0ccb33173adb6c2aeb69a814265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725699"
---
# <a name="helpcontextid-property-commands-collection-object"></a>HelpContextID, propriété (objet collection Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit un numéro de contexte associé pour l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Utilisé pour fournir une aide contextuelle pour l’objet **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Commandes («_*_nom_*_»)._ *  \[  =  *Numéro* de la HelpContextID\]



| Partie     | Description                                   |
|----------|-----------------------------------------------|
| *Nombre* | Entier spécifiant un numéro de contexte valide. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **True** et que l’utilisateur sélectionne l’objet [**commands**](/windows/desktop/lwef/the-commands-collection-object) . Si vous définissez un numéro de contexte dans la **HelpContextID**, l’agent appelle l’aide et recherche la rubrique identifiée par ce numéro de contexte.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> la génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**HelpFile, propriété**](helpfile-property.md)


 

 
