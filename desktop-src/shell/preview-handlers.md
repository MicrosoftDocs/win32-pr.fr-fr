---
description: Les gestionnaires d’aperçus sont appelés lorsqu’un élément est sélectionné pour afficher un aperçu léger, enrichi et en lecture seule du contenu du fichier dans le volet de lecture de la vue. Cette opération est effectuée sans lancer l’application associée au fichier.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Gestionnaires d’aperçus et hôte de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973351"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Gestionnaires d’aperçus et hôte de l’interpréteur de commandes

Les gestionnaires d’aperçus sont appelés lorsqu’un élément est sélectionné pour afficher un aperçu léger, enrichi et *en lecture seule* du contenu du fichier dans le volet de lecture de la vue. Cette opération est effectuée sans lancer l’application associée au fichier.

Cette rubrique aborde les sujets suivants :

-   [Architecture du gestionnaire d’aperçus](#preview-handler-architecture)
-   [Options du modèle de serveur](#server-model-options)
-   [Initialisation](#initialization)
-   [Aperçu du workflow du gestionnaire de données](#preview-handler-data-flow)
-   [Débogage d’un gestionnaire d’aperçus](#debugging-a-preview-handler)
-   [Fournir votre propre processus pour un gestionnaire d’aperçus](#providing-your-own-process-for-a-preview-handler)
-   [Rubriques connexes](#related-topics)

## <a name="preview-handler-architecture"></a>Architecture du gestionnaire d’aperçus

Un gestionnaire d’aperçus est une application hébergée. Les ordinateurs hôtes incluent l’Explorateur Windows dans Windows Vista ou Microsoft Outlook 2007. Les hôtes implémentent [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) comme méthode de communication entre le gestionnaire d’aperçus et l’hôte.

Le gestionnaire d’aperçus lui-même implémente les interfaces suivantes :

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (facultatif)

Votre gestionnaire est appelé par le biais de son [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), qui retourne un pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) par le biais duquel vous demandez à un objet [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) d’interagir avec l’hôte.

## <a name="server-model-options"></a>Options du modèle de serveur

Les gestionnaires d’aperçus sont toujours exécutés hors processus. Il existe deux méthodes d’implémentation de ce qui suit :

1.  Un gestionnaire d’aperçus peut être généré en tant que serveur in-process, mais exécuté via un hôte de substitution hors processus. Ceci est la méthode privilégiée. Le système fournit un hôte de substitution pour cela dans le fichier Prevhost.exe. Les gestionnaires d’aperçus créés par cette méthode ne sont pas compatibles avec Outlook 2007 sur Windows XP. Toutefois, ces mêmes gestionnaires fonctionneront dans l’Explorateur Windows et Outlook 2007 s’exécutant sur Windows Vista.
2.  Un gestionnaire d’aperçus peut être créé en tant que serveur COM (Component Object Model) local. Cela n’est pas recommandé pour plusieurs raisons. Tout d’abord, il est plus facile d’implémenter un serveur in-process. Plus important encore, l’implémentation en tant que serveur in-process offre un contrôle accru sur la durée de vie de l’objet gestionnaire, ce qui permet un nettoyage et une efficacité améliorés.

Par défaut, les gestionnaires d’aperçus s’exécutent dans un processus de niveau d’intégrité faible pour des raisons de sécurité. Vous pouvez éventuellement désactiver l’exécution comme un processus de langage intermédiaire faible en définissant la valeur suivante dans le registre. Toutefois, il n’est pas recommandé de le faire. Les systèmes peuvent finalement être configurés pour rejeter tout processus qui n’est pas de niveau IL faible.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Les différents gestionnaires d’aperçus partagent le même processus par défaut. Deux instances de Prevhost.exe peuvent s’exécuter simultanément ; un pour les gestionnaires s’exécutant en tant que processus IL bas, un pour les gestionnaires qui n’ont pas choisi ce comportement.

## <a name="initialization"></a>Initialisation

Comme avec les gestionnaires de miniatures et de propriétés, il est fortement recommandé d’initialiser votre gestionnaire avec un flux. Vous pouvez initialiser un fichier ou un élément si nécessaire, mais les flux fournissent la méthode la plus sûre pour implémenter un gestionnaire. L’initialisation via un flux garantit l’intégrité des fichiers et les avantages de la stabilité du système d’exécution du gestionnaire comme un processus de langage intermédiaire faible, par exemple la protection du système contre les dépassements de mémoire tampon, la limitation de l’endroit où un gestionnaire peut écrire des informations et la limitation de la communication avec d’autres fenêtres.

Si vous devez initialiser avec un fichier ou un élément de Shell, stockez le chemin d’accès du fichier ou une référence à [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). Ne lisez pas les données de ces sources tant que [**IPreviewHandler ::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) n’est pas appelé.

En général, l’initialisation ne doit pas effectuer de tâches lourdes telles que la composition et le stockage d’une image d’aperçu. Pour une efficacité optimale, ce type de traitement ne doit pas être effectué tant que l’aperçu n’est pas appelé pour.

## <a name="preview-handler-data-flow"></a>Aperçu du workflow du gestionnaire de données

Le workflow du processus d’aperçu suit le chemin d’accès général indiqué ici. L’hôte peut être considéré comme l’Explorateur Windows dans Windows Vista ou Outlook 2007.

1.  Le gestionnaire d’aperçus est initialisé, de préférence avec un flux.
2.  La fenêtre d’affichage est passée de l’hôte au gestionnaire via [**IPreviewHandler :: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  À ce stade, le gestionnaire ne doit faire rien d’autre tant que [**IPreviewHandler ::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) n’est pas appelé.
4.  L’aperçu s’affiche dans le volet de lecture via un appel à [**IPreviewHandler ::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  La taille de la fenêtre est définie par le biais de [**IPreviewHandler :: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  La fenêtre est redimensionnée lorsque nécessaire via [**IPreviewHandler :: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  L’aperçu est déchargé et ses ressources sont libérées lorsqu’il n’est plus nécessaire, par le biais d’un appel à [**IPreviewHandler :: Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Débogage d’un gestionnaire d’aperçus

Si vous avez suivi les recommandations pour implémenter votre gestionnaire d’aperçus en tant que serveur in-process, pour déboguer votre gestionnaire d’aperçus, vous pouvez attacher à Prevhost.exe. Comme mentionné précédemment, n’oubliez pas qu’il peut y avoir deux instances de Prevhost.exe, une pour les processus de langage intermédiaire basse normale et une pour les gestionnaires qui n’ont pas été exécutés comme un processus de langage intermédiaire faible.

Si vous ne trouvez pas Prevhost.exe dans votre liste de processus disponibles, cela signifie probablement qu’il n’a pas été chargé à ce stade. Si vous cliquez sur un fichier pour un aperçu, le substitut est chargé et il doit apparaître comme un processus pouvant être attaché.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Fournir votre propre processus pour un gestionnaire d’aperçus

Si vous souhaitez forcer la création d’un nouveau processus pour votre gestionnaire au lieu d’exécuter le processus par défaut, créez une nouvelle sous-clé pour votre gestionnaire sous **AppID** et définissez son entrée DllSurrogate sur « Prevhost.exe ». Utilisez cette sous-clé **AppID** à la place de la valeur par défaut Prevhost.exe **AppID**.

En fournissant un nouveau processus, le gestionnaire peut éviter de s’exécuter sous un processus partagé, comme c’est le cas par défaut. Cela peut vous permettre, par exemple, de garantir la version spécifique du common language runtime (CLR) dans le processus. Cela est nécessaire si vous générez une implémentation managée d’un gestionnaire d’aperçus.

> [!Note]  
> les gestionnaires d’aperçus 32 bits doivent utiliser **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} lorsqu’ils sont installés sur des systèmes d’exploitation 64 bits.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de gestionnaires d’aperçus](building-preview-handlers.md)
</dt> <dt>

[Comment inscrire un gestionnaire d’aperçus](how-to-register-a-preview-handler.md)
</dt> <dt>

[Instructions du gestionnaire d’aperçus](preview-handler-guidelines.md)
</dt> </dl>

 

 
