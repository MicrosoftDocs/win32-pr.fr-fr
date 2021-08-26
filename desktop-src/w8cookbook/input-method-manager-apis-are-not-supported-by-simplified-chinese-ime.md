---
title: Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié
description: Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935409"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Les API du gestionnaire de méthode d’entrée suivantes ne sont pas prises en charge par les éditeurs IME chinois simplifié dans Windows 8.1 :

-   Interface IFECommon
-   Interface IFEDictionary
-   Interface IFELanguage
-   Interface IImePad
-   Interface IImePadApplet
-   Interface IImeSpecifyApplets

## <a name="manifestations"></a>Manifestations

Les fonctions qui utilisent ces API ne fonctionnent pas avec l’éditeur IME chinois simplifié.

## <a name="solution"></a>Solution

Les applications doivent être conçues pour que les utilisateurs puissent terminer la tâche souhaitée sans utiliser l’API spécifiée.

## <a name="resources"></a>Ressources

-   [Interfaces du gestionnaire de méthode d’entrée](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interface IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interface IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 