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
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="f5087-103">Bibliothèque COM et contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f5087-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="f5087-104">Cette section décrit comment configurer votre environnement pour utiliser les bibliothèques COM de plateforme Tablet PC en C++.</span><span class="sxs-lookup"><span data-stu-id="f5087-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="f5087-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="f5087-105">Microsoft Visual C++</span></span>

<span data-ttu-id="f5087-106">Pour créer des applications Tablet PC dans Visual C++, vous devez mettre à jour les variables d’environnement système, configurer les options d’annuaire pour Visual Studio et accéder aux interfaces Tablet PC dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="f5087-107">Pour mettre à jour les variables d’environnement, suivez les instructions fournies par le SDK Windows pour l’ajout de variables d’environnement à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f5087-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="f5087-108">Accès aux interfaces Tablet PC</span><span class="sxs-lookup"><span data-stu-id="f5087-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="f5087-109">Pour accéder aux interfaces Tablet PC, vous devez inclure les fichiers Msinkaut. h et Msinkaut \_ i. c dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="f5087-110">Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include mentionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="f5087-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="f5087-111">Pour accéder aux interfaces InkAnalysis, vous devez inclure les fichiers IACom. h et IACom \_ i. c dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="f5087-112">Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include mentionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="f5087-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="f5087-113">Pour accéder aux interfaces [**InkDivider**](inkdivider-class.md) , vous devez inclure les \_ fichiers msinkaut15 i. c et msinkaut15. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="f5087-114">InkDivider a été remplacé par les API d’analyse d’encre.</span><span class="sxs-lookup"><span data-stu-id="f5087-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="f5087-115">Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include.</span><span class="sxs-lookup"><span data-stu-id="f5087-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="f5087-116">Pour accéder aux interfaces [**PenInputPanel**](peninputpanel-class.md) , vous devez inclure les \_ fichiers PenInputPanel i. c et PenInputPanel. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="f5087-117">Vous pouvez également utiliser la directive d’importation suivante à la place des \# instructions include.</span><span class="sxs-lookup"><span data-stu-id="f5087-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="f5087-118">Les API PenInputPanel ont été remplacées dans Windows Vista par les nouvelles interfaces du panneau de saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="f5087-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="f5087-119">Pour accéder aux interfaces de contrôle [InkEdit](inkedit-control-reference.md) , vous devez inclure les fichiers. h et les fichiers. c de l’entrée manuscrite \_ dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f5087-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="f5087-120">Vous pouvez également \# importer le fichier InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="f5087-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



