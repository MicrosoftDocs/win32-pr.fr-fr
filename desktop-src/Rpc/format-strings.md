---
title: Chaînes de format
description: Une chaîne de format est un jeton interprété que le moteur de NDR comprend. Les chaînes de format sont souvent appelées éléments MOP ; Cette documentation utilise le terme chaîne de format dans tout.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8c14fa649e71411c5706193e83fd9a09d30f8a0c57fec411d8c34fef675ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929866"
---
# <a name="format-strings"></a>Chaînes de format

Une chaîne de format est un jeton interprété que le moteur de NDR comprend. Les chaînes de format sont souvent appelées éléments MOP ; Cette documentation utilise le terme chaîne de format dans tout.

Pour être plus précis, un caractère de format est un jeton interprétable (atomique) individuel. Chaque caractère de format est d’une taille d’un octet. Une chaîne de format est une séquence de caractères de format ou de caractères de format et de données numériques. Le descripteur de terme est également utilisé pour nommer des séquences courantes. par exemple, une chaîne de format de paramètre ou un descripteur de paramètre est une chaîne de format utilisée pour décrire un paramètre d’une routine.

Les caractères de format ont des noms symboliques de type « Fibre Channel » \_ ou « struct FC » \_ . Tous les caractères de chaîne de format utilisés par MIDL et le moteur de NDR sont définis dans le fichier Ndrtypes. h.

## <a name="format-string-tables"></a>Tables de chaînes de format

Deux tables de chaînes de format principales sont utilisées par le moteur : la table de format de procédure, **\_ \_ MIDL \_ ProcFormatString**, qui conserve les descripteurs de procédure ; et la table de chaînes de format de type, **\_ \_ MIDL \_ TypeFormatString**, qui conserve les descripteurs de type de données. Le compilateur génère les deux dans les fichiers stub principaux ( \* \_ c. c, \* \_ s. c, \* \_ p. c). La table de chaînes de format de procédure est utilisée principalement par différents interpréteurs, mais elle est également utilisée pour la conversion de mémoire tampon, quel que soit le mode du compilateur. Le type de table de chaînes de format est utilisé lors de l’appel du moteur de rapport de données principal pour indiquer les types de données spécifiques sur lesquels travailler.

## <a name="format-string-notation"></a>Notation de chaîne de format

La notation utilisée dans ce document suit des indications de description de programmation courantes, avec une barre ( \| ) utilisée pour désigner d’autres constructions et crochets ( \[ \] ) utilisés pour indiquer des éléments facultatifs. Les chaînes de format sont fréquemment empilées pour des raisons de lisibilité (responsabilisation). Dans ce document, FC désigne un caractère de format unique. Les caractères de format sont présentés en MAJUSCULEs, à l’aide de leurs noms symboliques réels. D’autres champs arbitraires sont représentés par un nom et une taille.

Les chevrons ( <> ) sont utilisés pour indiquer la taille des descripteurs. Les conventions présentées dans le tableau suivant sont utilisées.



| Notation     | Signification                                                   |
|--------------|-----------------------------------------------------------|
| <*n*>  | La taille du descripteur est de n octets.                        |
| <>     | La taille du descripteur varie.                            |
| {<>}\* | Le descripteur est répété un nombre quelconque de fois (0, 1, 2...). |



 

Les caractères de format suivants ont une signification particulière.



| Caractère | Signification                                   |
|-----------|-------------------------------------------|
| \_fin FC   | Indique la fin de certaines chaînes de format. |
| \_boîtier FC   | Caractère de remplissage non interprété.              |



 

 

 




