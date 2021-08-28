---
description: Cette section décrit comment configurer votre environnement pour utiliser les bibliothèques COM de plateforme Tablet PC en C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: bibliothèque COM et contrôles de ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bc76f9caa2bcb72fe26ed2e01e251c977f87ce01c12794aad78608d2f5887f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009089"
---
# <a name="com-library-and-activex-controls"></a>bibliothèque COM et contrôles de ActiveX

Cette section décrit comment configurer votre environnement pour utiliser les bibliothèques COM de plateforme Tablet PC en C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

pour créer des applications Tablet pc dans Visual C++, vous devez mettre à jour les variables d’environnement système, configurer les options de répertoire pour les Visual Studio et accéder aux interfaces Tablet pc dans votre projet.

pour mettre à jour les variables d’environnement, suivez les instructions fournies par le SDK Windows pour l’ajout de variables d’environnement à Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Accès aux interfaces Tablet PC

Pour accéder aux interfaces Tablet PC, vous devez inclure les fichiers Msinkaut. h et Msinkaut \_ i. c dans votre projet.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include mentionnées précédemment.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Pour accéder aux interfaces InkAnalysis, vous devez inclure les fichiers IACom. h et IACom \_ i. c dans votre projet.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include mentionnées précédemment.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Pour accéder aux interfaces [**InkDivider**](inkdivider-class.md) , vous devez inclure les \_ fichiers msinkaut15 i. c et msinkaut15. h dans votre projet.

> [!Note]  
> InkDivider a été remplacé par les API d’analyse d’encre.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Pour accéder aux interfaces [**PenInputPanel**](peninputpanel-class.md) , vous devez inclure les \_ fichiers PenInputPanel i. c et PenInputPanel. h dans votre projet.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> les api PenInputPanel ont été remplacées dans Windows Vista par les nouvelles interfaces du panneau de saisie de texte.

 

Pour accéder aux interfaces de contrôle [InkEdit](inkedit-control-reference.md) , vous devez inclure les fichiers. h et les fichiers. c de l’entrée manuscrite \_ dans votre projet.


```C++
#include <inked.h>
#include <inked_i.c>
```



Vous pouvez également \# importer le fichier InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



