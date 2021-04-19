---
description: Montre comment utiliser les interfaces VSS pour créer un fournisseur de matériel VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Outil et exemple VssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517502"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Outil et exemple VssSampleProvider

Montre comment utiliser les [interfaces](volume-shadow-copy-api-interfaces.md) VSS pour créer un fournisseur de matériel VSS.

> [!Note]  
> L’outil et l’exemple VssSampleProvider sont inclus dans le kit de développement logiciel (SDK) Microsoft Windows. Vous pouvez télécharger le SDK Windows à partir du [Kit de développement logiciel (SDK) Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

Dans l’installation SDK Windows, l’outil VssSampleProvider se trouve dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour Windows 32 bits).

> [!Note]  
> Les fournisseurs de matériel sont uniquement pris en charge sur les systèmes d’exploitation Windows Server. Sur un système d’exploitation client Windows, vous pouvez compiler l’exemple VssSampleProvider, mais vous ne pouvez pas l’inscrire en tant que fournisseur de matériel.

 

L’outil VssSampleProvider se compose des fichiers suivants :

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

L’exemple VssSampleProvider comprend les scripts d’installation et de désinstallation suivants :

-   Install-SampleProvider. cmd
-   Uninstall-SampleProvider. cmd
-   Inscrire \_app.vbs

**Pour installer et utiliser l’exemple VssSampleProvider**

1.  Accédez au répertoire `Program Files (x86)\Windows Kits\8.0\bin\`. Ce répertoire contient virtualstoragevss.sys et vstorcontrol.exe.
2.  Ouvrez une fenêtre d’invite de commandes dans le répertoire spécifié.
3.  Pour installer le pilote de stockage virtuel, dans la fenêtre d’invite de commandes, tapez la commande suivante :

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Pour installer l’exemple de fournisseur VSS, dans la fenêtre d’invite de commandes, tapez la commande suivante :

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Pour créer un numéro d’unité logique virtuelle, procédez comme suit.

    1.  Dans la fenêtre d’invite de commandes, tapez la commande suivante :

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Cette commande crée un LUN virtuel dont l’identificateur de stockage est le **fournisseur d’exemples de matériel VSS**. Pour créer des numéros d’unités logiques virtuels supplémentaires, répétez cette étape.

        L’exemple de fournisseur VSS reconnaît un numéro d’unité logique uniquement si le **fournisseur de matériel exemple VSS** fait partie de l’identificateur de stockage. Pour plus d’informations sur l’identificateur de stockage, consultez le billet de blog suivant.

        [LUN-resynchronisation avec DiskShadow et le stockage virtuel](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Dans la fenêtre d’invite de commandes, utilisez diskpart.exe pour formater le disque virtuel et lui attribuer une lettre de lecteur.

        Voici un exemple de script à exécuter à l’invite de commandes Diskpart.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Pour exécuter l’exemple de fournisseur, dans la fenêtre d’invite de commandes, tapez la commande suivante :

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *<drive>* représente la lettre de lecteur du numéro d’unité logique virtuelle.

7.  Pour désinstaller l’exemple de fournisseur VSS, dans la fenêtre d’invite de commandes, tapez la commande suivante :

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Pour désinstaller le pilote de stockage virtuel, dans la fenêtre d’invite de commandes, tapez la commande suivante :

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



