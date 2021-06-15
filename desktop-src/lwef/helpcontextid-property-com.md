---
title: HelpContextID, propriété (objet Command)
description: En savoir plus sur la propriété HelpContextID de l’objet Command. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068508"
---
# <a name="helpcontextid-property-command-object"></a>HelpContextID, propriété (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit un numéro de contexte associé pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . Utilisé pour fournir une aide contextuelle pour l’objet de **commande** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Commandes («»)._ *  \[  =  *Numéro* de la HelpContextID\]



| Partie     | Description                                   |
|----------|-----------------------------------------------|
| *Nombre* | Entier spécifiant un numéro de contexte valide. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère sur le fichier, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande. Si vous définissez un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**HelpFile, propriété**](helpfile-property.md)


 

 
