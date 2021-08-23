---
title: installation et inscription de gestionnaires de protocole (fonctionnalités d’environnement de Windows héritées)
description: L’installation de gestionnaires de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files et leur inscription.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716559"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>installation et inscription de gestionnaires de protocole (fonctionnalités d’environnement de Windows héritées)

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

L’installation de **gestionnaires de protocole** implique la copie de la ou des dll vers un emplacement approprié dans le répertoire Program Files et leur inscription.

Cette section contient les rubriques suivantes :

-   [Instructions d’installation](#installation-guidelines)
-   [Pour inscrire des gestionnaires de protocole](#to-register-protocol-handlers)
-   [Pour inscrire des extensions de Shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Instructions d’installation

Les gestionnaires de protocole doivent implémenter l’inscription automatique pour l’installation et doivent suivre les instructions suivantes :

-   Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.
-   Des notes de publication doivent être fournies.
-   Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.
-   Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.
-   Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.
-   Si un complément plus récent a remplacé le complément précédent, il doit être possible de restaurer les fonctionnalités précédentes du complément et de faire de nouveau le complément par défaut pour ce type de fichier.

## <a name="to-register-protocol-handlers"></a>Pour inscrire des gestionnaires de protocole

Vous devez faire quatorze entrées dans le registre pour inscrire le composant de gestionnaire de protocole, où :

-   *Ver \_ IND \_ ProgID* est le ProgID indépendant de la version de l’implémentation du gestionnaire de protocole
-   *Ver \_ \_ProgID DEP* est le ProgID dépendant de la version de l’implémentation du gestionnaire de protocole
-   *CLSID \_ 1* est le CLSID de l’implémentation du gestionnaire de protocole

1.  Enregistrez le ProgID indépendant de la version avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  Enregistrez le ProgID dépendant de la version avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Enregistrez le CLSID du gestionnaire de protocole avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  inscrire le gestionnaire de protocole avec Windows Desktop Search :

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>Pour inscrire des extensions de Shell

Vous devez créer deux entrées dans le registre pour enregistrer l’extension d’interpréteur de commandes du gestionnaire de protocole.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




