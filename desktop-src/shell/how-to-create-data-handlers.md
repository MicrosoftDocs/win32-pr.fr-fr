---
description: Extension du presse-papiers avec des gestionnaires de format de données personnalisés.
title: Comment créer des gestionnaires de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991565"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="9bd00-103">Comment créer des gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="9bd00-103">How to Create Data Handlers</span></span>

<span data-ttu-id="9bd00-104">Lorsqu’un fichier est copié dans le presse-papiers ou glissé et déposé, le shell crée un objet de données qui prend en charge un large éventail de [formats de presse-papiers](dragdrop.md)standard.</span><span class="sxs-lookup"><span data-stu-id="9bd00-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="9bd00-105">Pour les fichiers qui sont d’un type de fichier spécifique, vous pouvez étendre les formats de presse-papiers disponibles en implémentant et en inscrivant un *Gestionnaire de données*.</span><span class="sxs-lookup"><span data-stu-id="9bd00-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="9bd00-106">Lorsqu’un fichier du type de fichier est transféré, l’interpréteur de commandes délègue les appels à l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données au gestionnaire de données si l’un des formats personnalisés est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9bd00-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="9bd00-107">Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9bd00-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="9bd00-108">Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de données.</span><span class="sxs-lookup"><span data-stu-id="9bd00-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="9bd00-109">Implémentation de gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="9bd00-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="9bd00-110">Inscription des gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="9bd00-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="9bd00-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bd00-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="9bd00-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="9bd00-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="9bd00-113">Étape 1 : implémentation des gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="9bd00-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="9bd00-114">Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de données sont des objets COM (Component Object Model) in-process implémentés en tant que dll.</span><span class="sxs-lookup"><span data-stu-id="9bd00-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="9bd00-115">Elles exportent deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) et [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="9bd00-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="9bd00-116">L’interpréteur de commandes Initialise le gestionnaire via son interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="9bd00-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="9bd00-117">Elle utilise cette interface pour demander l’identificateur de classe du gestionnaire (CLSID) et lui fournit le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="9bd00-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="9bd00-118">Pour obtenir une description générale de l’implémentation des gestionnaires d’extensions de Shell, y compris l’interface **IPersistFile** , consultez [création de gestionnaires d’extension de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9bd00-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="9bd00-119">Une fois le gestionnaire de données initialisé, l’interpréteur de commandes délègue les appels de l’objet de données à l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) du gestionnaire si l’un des formats personnalisés est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9bd00-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="9bd00-120">Étape 2 : inscription des gestionnaires de données</span><span class="sxs-lookup"><span data-stu-id="9bd00-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="9bd00-121">Les gestionnaires de données sont enregistrés sous la sous-clé *ProgID* du type de fichier comme indiqué ici : **HKEY \_ classes \_ root** \\ *ProgID* \\ **shellex** \\ **DataHandler**</span><span class="sxs-lookup"><span data-stu-id="9bd00-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="9bd00-122">Créez une sous-clé nommée pour le gestionnaire sous **DataHandler** et définissez la valeur par défaut de la sous-clé de ce gestionnaire sur la forme de chaîne du GUID CLSID du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="9bd00-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="9bd00-123">Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9bd00-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="9bd00-124">L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire de données pour un exemple de type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="9bd00-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="9bd00-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bd00-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd00-126">Création de gestionnaires d’extensions d’environnement</span><span class="sxs-lookup"><span data-stu-id="9bd00-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="9bd00-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="9bd00-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="9bd00-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="9bd00-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
