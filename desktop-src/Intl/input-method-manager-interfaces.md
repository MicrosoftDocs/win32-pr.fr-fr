---
description: Cette section décrit les interfaces IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces du gestionnaire de méthode d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e7267f5f38bb160a7f71b4f0379a2b03a3263b85a64dc8e666226dd3150911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809998"
---
# <a name="input-method-manager-interfaces"></a>Interfaces du gestionnaire de méthode d’entrée

Cette section décrit les interfaces IMM.



| Interface                                                            | Description                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Fournit des services liés à l’IME qui sont communs aux différents langages.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Permet aux clients d’accéder à un dictionnaire utilisateur Microsoft IME.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Fournit des services de traitement de langage à l’aide de l’éditeur IME Microsoft.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Insère du texte dans des applications à partir de IMEPadApplets qui implémentent l’interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Saisit des chaînes dans les applications via l’interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Permet d’accéder à la liste des dictionnaires de plug-in IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Spécifie les méthodes appelées à partir de l’objet d’interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) pour émuler l’interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) . |



 

 

 



