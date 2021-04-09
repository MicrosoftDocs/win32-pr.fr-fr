---
title: Fichiers IDL
description: Fichiers IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842781"
---
# <a name="idl-files"></a>Fichiers IDL

COM utilise le Microsoft Interface Definition Language (MIDL) pour décrire les objets COM. MIDL est une extension de l’IDL pour les environnements informatiques distribués définis par Open Software Foundation, qui a été développé pour définir les interfaces des appels de procédure distante dans les applications client/serveur traditionnelles. MIDL comprend la plupart des attributs et des instructions du langage ODL (Object Definition Language), le langage utilisé à l’origine pour générer des bibliothèques de types pour OLE Automation.

En C++ et Java, un développeur créant un objet COM crée un fichier IDL que le compilateur MIDL traite ensuite pour créer une bibliothèque de types ou des fichiers d’en-tête et de proxy, ou les deux. Une *bibliothèque de types* est un fichier binaire qui décrit l’objet com ou les interfaces com, ou les deux. Une bibliothèque de types est la version compilée du fichier IDL. Toutefois, les bibliothèques de types prennent uniquement en charge la sémantique ODL. En particulier, ils ne peuvent pas représenter toutes les informations d’un fichier IDL lié aux attributs IDL, par exemple la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) \] . Vous devez créer et utiliser des fichiers de proxy pour les fichiers IDL affectés par la perte d’informations dans la bibliothèque de types.

Dans Visual Basic, un développeur qui crée un objet COM ne crée pas de fichier IDL. Au lieu de cela, Visual Basic recueille des informations à l’aide des propriétés de classe et de projet et crée directement la bibliothèque de types.

 

 