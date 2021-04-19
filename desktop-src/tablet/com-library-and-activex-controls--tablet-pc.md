---
description: Cette section décrit comment configurer votre environnement pour utiliser les bibliothèques COM de plateforme Tablet PC en C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Bibliothèque COM et contrôles ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515197"
---
# <a name="com-library-and-activex-controls"></a>Bibliothèque COM et contrôles ActiveX

Cette section décrit comment configurer votre environnement pour utiliser les bibliothèques COM de plateforme Tablet PC en C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Pour créer des applications Tablet PC dans Visual C++, vous devez mettre à jour les variables d’environnement système, configurer les options d’annuaire pour Visual Studio et accéder aux interfaces Tablet PC dans votre projet.

Pour mettre à jour les variables d’environnement, suivez les instructions fournies par le SDK Windows pour l’ajout de variables d’environnement à Visual Studio.

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
> Les API PenInputPanel ont été remplacées dans Windows Vista par les nouvelles interfaces du panneau de saisie de texte.

 

Pour accéder aux interfaces de contrôle [InkEdit](inkedit-control-reference.md) , vous devez inclure les fichiers. h et les fichiers. c de l’entrée manuscrite \_ dans votre projet.


```C++
#include <inked.h>
#include <inked_i.c>
```



Vous pouvez également \# importer le fichier InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



