---
title: Installation de l’exemple de composant fournisseur
description: Après avoir installé le kit de développement logiciel (SDK) ADSI, dans le répertoire d’installation, accédez au sous-répertoire Samples \\ NetDs \\ ADSI \\ Samples \\ \\ Setup. Exécutez Install.bat comme décrit dans le fichier README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installation de l’exemple d’interface ADSI du composant fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333239"
---
# <a name="installing-the-example-provider-component"></a>Installation de l’exemple de composant fournisseur

Après avoir installé le kit de développement logiciel (SDK) ADSI, dans le répertoire d’installation, accédez au sous-répertoire Samples \\ NetDs \\ ADSI \\ Samples \\ \\ Setup. Exécutez Install.bat comme décrit dans le fichier README.TXT.

L’exemple de fournisseur ADSI ajoutera les sous-clés et les valeurs suivantes au registre lors de l’exécution de Install.bat fichier :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

D’autres entrées de Registre existent pour le composant de fournisseur d’exemple, car l’exemple de composant de fournisseur implémente sa hiérarchie de répertoires dans le registre. Cela implique en aucun cas que d’autres fournisseurs souhaiteraient ou devraient faire de même.

 

 




