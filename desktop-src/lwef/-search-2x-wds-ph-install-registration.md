---
title: Installation et inscription de gestionnaires de protocole (fonctionnalités d’environnement Windows héritées)
description: L’installation de gestionnaires de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files et leur inscription.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317082"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="ce886-103">Installation et inscription de gestionnaires de protocole (fonctionnalités d’environnement Windows héritées)</span><span class="sxs-lookup"><span data-stu-id="ce886-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="ce886-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce886-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ce886-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="ce886-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="ce886-106">L’installation de **gestionnaires de protocole** implique la copie de la ou des dll vers un emplacement approprié dans le répertoire Program Files et leur inscription.</span><span class="sxs-lookup"><span data-stu-id="ce886-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="ce886-107">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce886-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="ce886-108">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="ce886-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="ce886-109">Pour inscrire des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="ce886-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="ce886-110">Pour inscrire des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="ce886-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="ce886-111">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="ce886-111">Installation Guidelines</span></span>

<span data-ttu-id="ce886-112">Les gestionnaires de protocole doivent implémenter l’inscription automatique pour l’installation et doivent suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce886-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="ce886-113">Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.</span><span class="sxs-lookup"><span data-stu-id="ce886-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="ce886-114">Des notes de publication doivent être fournies.</span><span class="sxs-lookup"><span data-stu-id="ce886-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="ce886-115">Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.</span><span class="sxs-lookup"><span data-stu-id="ce886-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="ce886-116">Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.</span><span class="sxs-lookup"><span data-stu-id="ce886-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="ce886-117">Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce886-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="ce886-118">Si un complément plus récent a remplacé le complément précédent, il doit être possible de restaurer les fonctionnalités précédentes du complément et de faire de nouveau le complément par défaut pour ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="ce886-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="ce886-119">Pour inscrire des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="ce886-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="ce886-120">Vous devez faire quatorze entrées dans le registre pour inscrire le composant de gestionnaire de protocole, où :</span><span class="sxs-lookup"><span data-stu-id="ce886-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="ce886-121">*Ver \_ IND \_ ProgID* est le ProgID indépendant de la version de l’implémentation du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="ce886-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="ce886-122">*Ver \_ \_ProgID DEP* est le ProgID dépendant de la version de l’implémentation du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="ce886-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="ce886-123">*CLSID \_ 1* est le CLSID de l’implémentation du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="ce886-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="ce886-124">Enregistrez le ProgID indépendant de la version avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce886-124">Register the version independent ProgID with the following keys and values:</span></span>

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

2.  <span data-ttu-id="ce886-125">Enregistrez le ProgID dépendant de la version avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce886-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="ce886-126">Enregistrez le CLSID du gestionnaire de protocole avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce886-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

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

4.  <span data-ttu-id="ce886-127">Inscrire le gestionnaire de protocole auprès de Windows Desktop Search :</span><span class="sxs-lookup"><span data-stu-id="ce886-127">Register the protocol handler with Windows Desktop Search:</span></span>

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

## <a name="to-register-shell-extensions"></a><span data-ttu-id="ce886-128">Pour inscrire des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="ce886-128">To Register Shell Extensions</span></span>

<span data-ttu-id="ce886-129">Vous devez créer deux entrées dans le registre pour enregistrer l’extension d’interpréteur de commandes du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="ce886-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




