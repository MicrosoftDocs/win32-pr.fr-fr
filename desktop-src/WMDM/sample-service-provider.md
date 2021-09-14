---
title: Exemple de fournisseur de services
description: Exemple de fournisseur de services
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Gestionnaire de périphériques de média, exemples
- Gestionnaire de périphériques, exemples
- Windows Gestionnaire de périphériques de support, exemple de fournisseur de services
- Gestionnaire de périphériques, exemple de fournisseur de services
- fournisseurs de services, exemples
- exemples, fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414575"
---
# <a name="sample-service-provider"></a>Exemple de fournisseur de services

le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques comprend un exemple de fournisseur de services que vous pouvez utiliser. Ce fournisseur de services comprend une classe qui signale chaque disque dur de l’ordinateur comme s’il s’agissait d’un appareil attaché. La seule application qui utilisera ce fournisseur de services est l’exemple d’application ; Windows L’Explorateur ne voit pas les « périphériques » signalés par ce fournisseur de services. L’exemple de fournisseur de services est un objet COM basé sur ATL. Les étapes suivantes expliquent comment utiliser l’exemple de fournisseur de services :

> [!Note]  
> l’exemple de fournisseur de services implémente très peu de fonctionnalités. il ne doit donc pas être utilisé pour tester des applications Windows Media Gestionnaire de périphériques. Pour tester une application, utilisez un fournisseur de services entièrement implémenté.

 

-   L’exemple a été fourni avec une erreur de codage qui entraînera un dysfonctionnement du fournisseur de services. Pour corriger cette erreur, ouvrez le fichier MDSPEnumStorage. cpp installé dans le dossier < *chemin d’installation du kit de développement logiciel (SDK)*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, accédez à la ligne 185, puis modifiez la ligne suivante :

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Par ceci :

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compilez le fichier MsHDSP.dll. Pour ce faire, vous pouvez utiliser NMAKE ou Visual Studio. consultez [compilation de l’exemple de fournisseur de services à l’aide de NMAKE](compiling-the-sample-service-provider-using-nmake.md) ou [compilation de l’exemple de fournisseur de services à l’aide de Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) pour savoir comment compiler l’application.
2.  Inscrivez MsHDSP.dll à l’aide de regsvr32. La ligne suivante, tapée dans une fenêtre d’invite de commandes dans le même dossier que MsHDSP.dll, inscrit l’exemple de fournisseur de services :

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Pour arrêter l’emprunt d’identité d’un appareil, entrez la ligne suivante à l’invite de commandes :

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Les appareils amovibles empruntés par cette DLL peuvent uniquement être vus par l’exemple d’application fourni avec ce kit de développement logiciel (SDK). Compilez l’exemple d’application à l’aide de l’une des méthodes décrites dans [exemple d’application de bureau](sample-desktop-application.md).
4.  pour déboguer le fournisseur de services avec Visual Studio, ouvrez le fournisseur de services dans Visual Studio et sélectionnez **démarrer** dans le menu **déboguer** . Dans la boîte de dialogue contextuelle, accédez à l’exemple d’application que vous avez créé à l’étape précédente, puis cliquez sur **OK**. le fournisseur de services commence alors à s’exécuter en mode débogage.

    pour exécuter le fournisseur de services sans débogage dans Visual Studio, il vous suffit d’inscrire le msdhsp.dll et d’exécuter l’exemple d’application de bureau fourni avec le kit de développement logiciel (SDK). L’exemple d’application de bureau exécute automatiquement l’exemple de fournisseur de services.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> </dl>

 

 




