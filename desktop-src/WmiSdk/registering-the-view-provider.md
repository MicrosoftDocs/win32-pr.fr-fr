---
description: WMI inscrit automatiquement la DLL du fournisseur d’affichage lors du processus d’installation de WMI. Toutefois, vous devez encore inscrire le fournisseur d’affichage auprès de WMI pour chaque espace de noms qui contiendra des classes d’affichage.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Inscription du fournisseur de vues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923360"
---
# <a name="registering-the-view-provider"></a>Inscription du fournisseur de vues

WMI inscrit automatiquement la DLL du fournisseur d’affichage lors du processus d’installation de WMI. Toutefois, vous devez encore inscrire le fournisseur d’affichage auprès de WMI pour chaque espace de noms qui contiendra des classes d’affichage.

La procédure suivante décrit comment inscrire le fournisseur d’affichage.

**Pour inscrire le fournisseur d’affichage**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour décrire l’implémentation du fournisseur d’affichage.

    L’instance [**\_ \_ Win32Provider**](--win32provider.md) décrit le nom du fournisseur et son identificateur de classe (CLSID), ainsi que les paramètres de sécurité par défaut.

    L’exemple de code suivant décrit une implémentation de [**\_ \_ Win32Provider**](--win32provider.md).

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

    L’exemple de code suivant montre comment créer une instance de la classe **\_ \_ InstanceProviderRegistration** .

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Créez une instance de la classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) si vous souhaitez que votre classe d’affichage Union prenne en charge des méthodes.

    L’exemple de code suivant montre comment créer une instance de la classe **\_ \_ MethodProviderRegistration** .

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compilez votre code MOF à l’aide du compilateur MOF ([mofcomp](mofcomp.md)) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Si vous enregistrez l’exemple de code MOF précédemment listé dans un fichier nommé Viewtest. mof, utilisez la commande mofcomp pour charger le code MOF dans l’espace de noms cible. *NamespacePath* est l’espace de noms dans lequel vous souhaitez créer l’instance de la classe d’affichage.

    Tapez la commande suivante à l’invite de commandes pour charger le code MOF dans l’espace de noms cible.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).

 

 



