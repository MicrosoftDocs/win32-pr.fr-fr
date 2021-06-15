---
title: HelpContextID, propriété (objet Characters)
description: En savoir plus sur la propriété HelpContextID de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068185"
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

Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère.

> [!Note]  
> La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**HelpFile, propriété**](helpfile-property.md)


 

 




