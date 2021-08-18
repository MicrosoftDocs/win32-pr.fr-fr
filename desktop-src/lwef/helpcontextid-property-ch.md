---
title: HelpContextID, propriété (objet Characters)
description: En savoir plus sur la propriété HelpContextID de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c790f4e3b0e69f4c8dc5e032b0021067e908f4af6200432dae668d08b47e1f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478716"
---
# <a name="helpcontextid-property-characters-object"></a>HelpContextID, propriété (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit un numéro de contexte associé pour le caractère. Utilisé pour fournir une aide contextuelle pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»)._ *  \[  =  *Numéro* de la HelpContextID\]



| Partie     | Description                                   |
|----------|-----------------------------------------------|
| *Nombre* | Entier spécifiant un numéro de contexte valide. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour prendre en charge l’aide contextuelle pour le caractère, assignez le numéro de contexte au caractère que vous utilisez pour la rubrique d’aide associée quand vous compilez votre fichier d’aide. Cette propriété s’applique uniquement au client du caractère ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères du client.

si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **True** et que l’utilisateur clique sur le caractère. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère.

> [!Note]  
> la génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**HelpFile, propriété**](helpfile-property.md)


 

 




