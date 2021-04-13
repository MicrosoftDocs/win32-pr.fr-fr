---
title: Installation de l’exemple de composant fournisseur
description: Après avoir installé le kit de développement logiciel (SDK) ADSI, dans le répertoire d’installation, accédez au sous-répertoire Samples \\ NetDs \\ ADSI \\ Samples \\ \\ Setup. Exécutez Install.bat comme décrit dans le fichier README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installation de l’exemple d’interface ADSI du composant fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0df567aa08b03ce9c043d345380f05cd6d1c20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379593"
---
# <a name="installing-the-example-provider-component"></a><span data-ttu-id="c97c5-105">Installation de l’exemple de composant fournisseur</span><span class="sxs-lookup"><span data-stu-id="c97c5-105">Installing the Example Provider Component</span></span>

<span data-ttu-id="c97c5-106">Après avoir installé le kit de développement logiciel (SDK) ADSI, dans le répertoire d’installation, accédez au sous-répertoire Samples \\ NetDs \\ ADSI \\ Samples \\ \\ Setup.</span><span class="sxs-lookup"><span data-stu-id="c97c5-106">After installing the ADSI SDK, from the installation directory, change directories to the Samples\\NetDs\\ADSI\\Samples\\Provider\\Setup subdirectory.</span></span> <span data-ttu-id="c97c5-107">Exécutez Install.bat comme décrit dans le fichier README.TXT.</span><span class="sxs-lookup"><span data-stu-id="c97c5-107">Run Install.bat as described in the README.TXT file.</span></span>

<span data-ttu-id="c97c5-108">L’exemple de fournisseur ADSI ajoutera les sous-clés et les valeurs suivantes au registre lors de l’exécution de Install.bat fichier :</span><span class="sxs-lookup"><span data-stu-id="c97c5-108">The sample ADSI provider will add the following subkeys and values to the registry when Install.bat file is run:</span></span>

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

<span data-ttu-id="c97c5-109">D’autres entrées de Registre existent pour le composant de fournisseur d’exemple, car l’exemple de composant de fournisseur implémente sa hiérarchie de répertoires dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c97c5-109">Other registry entries for the example provider component exist because the example provider component implemented its directory hierarchy in the registry.</span></span> <span data-ttu-id="c97c5-110">Cela implique en aucun cas que d’autres fournisseurs souhaiteraient ou devraient faire de même.</span><span class="sxs-lookup"><span data-stu-id="c97c5-110">This in no way implies other providers would want to or should do the same.</span></span>

 

 




