---
title: Manifeste de l’application (exécutable)
description: Manifeste de l’application (exécutable)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031985"
---
# <a name="app-executable-manifest"></a>Manifeste de l’application (exécutable)

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

La section compatibilité du manifeste de l’application (exécutable) introduite dans Windows permet au système d’exploitation de déterminer les versions de Windows qu’une application a été conçue pour cibler. En outre, le manifeste de l’application permet à Windows de fournir le comportement attendu par l’application en fonction de la version de Windows ciblée par l’application.

La section compatibilité du manifeste permet à Windows de fournir un nouveau comportement aux nouveaux logiciels tout en conservant la compatibilité des logiciels existants. Cette section permet également à Windows d’offrir une meilleure compatibilité dans les futures versions de Windows. Par exemple, une application qui déclare la prise en charge de Windows 8 uniquement dans la section compatibilité continuera à recevoir le comportement de Windows 8 dans les futures versions de Windows.

## <a name="manifestation"></a>Manifestation

Les applications sans section de compatibilité dans leur manifeste présentent le comportement de Windows Vista par défaut sur Windows 7 et Windows 8, ainsi que les versions futures de Windows. N’oubliez pas que Windows XP et Windows Vista ignorent cette section du manifeste et qu’il n’a aucun impact sur ces derniers.

Ces composants Windows fournissent un comportement divergent en fonction de la section compatibilité :

**Pool de threads par défaut de l’appel de procédure distante (RPC)**

-   Windows 8 et Windows 7 : pour améliorer l’évolutivité et réduire le nombre de threads, RPC bascule vers le pool de threads NT (pool par défaut). Pour Windows Vista, RPC utilisait un pool de threads privés :

    -   Pour les fichiers binaires compilés pour Windows 7 et les versions ultérieures de Windows, le pool par défaut est utilisé.
    -   Si I \_ RpcMgmtEnableDedicatedThreadPool est appelé avant l’appel d’une API RPC, le pool de threads privés est utilisé (comportement Vista).
    -   Si j' \_ RpcMgmtEnableDedicatedThreadPool est appelé après un appel RPC, le pool par défaut est utilisé, je \_ RpcMgmtEnableDedicatedThreadPool renvoie l’erreur 1764 et l’opération demandée n’est pas prise en charge.

-   Windows Vista (par défaut) : pour les fichiers binaires compilés pour Windows Vista et les versions antérieures de Windows, le pool privé est utilisé.

**Verrouillage DirectDraw**

-   Windows 8 et Windows 7 : les applications manifestées pour Windows 7 et les versions ultérieures du système d’exploitation ne peuvent pas appeler l’API Lock dans DDRAW pour verrouiller la mémoire tampon de la vidéo principale du bureau. Cela entraînera une erreur et un pointeur NULL pour le réplica principal est retourné. Ce comportement est appliqué même si Gestionnaire de fenêtrage composition n’est pas activée. Les applications dont la compatibilité est déclarée pour Windows 7 et les versions ultérieures ne doivent pas verrouiller la mémoire tampon vidéo principale à restituer.
-   Windows Vista (par défaut) : les applications peuvent acquérir un verrou sur la mémoire tampon vidéo principale, car les applications héritées dépendent de ce comportement. l’exécution de l’application désactive Gestionnaire de fenêtrage.

**Transfert de bloc de bits (BitBlt) DirectDraw vers le réplica principal sans fenêtre de découpage**

-   Windows 8 et Windows 7 : les applications manifestes pour Windows 7 et les versions ultérieures de Windows ne sont pas en mesure d’effectuer un BitBlt dans la mémoire tampon vidéo principale du bureau sans fenêtre de découpage ; Cela génère une erreur et la zone BitBlt ne s’affiche pas. Windows applique ce comportement même si vous n’activez pas la composition Gestionnaire de fenêtrage. Les applications dont la compatibilité est déclarée pour Windows 7 et les versions ultérieures doivent effectuer un BitBlt dans une fenêtre de découpage.
-   Windows Vista (par défaut) : les applications doivent être en mesure d’effectuer un BitBlt sur le serveur principal sans fenêtre de découpage, car les applications héritées dépendent de ce comportement. l’exécution de cette application désactive l’Gestionnaire de fenêtrage.

**API GetOverlappedResult**

-   Windows 8 et Windows 7 : résout une condition de concurrence dans laquelle une application multithread utilisant **GetOverlappedResult** peut retourner sans réinitialiser l’événement dans la structure OVERLAPPED, provoquant le retour prématuré de l’appel suivant à cette fonction.
-   Windows Vista (par défaut) : fournit le comportement avec la condition de concurrence sur laquelle les applications peuvent avoir une dépendance. Les applications qui doivent éviter cette concurrence avant le comportement de Windows 7 doivent attendre l’événement Overlapped et, lorsqu’elles sont signalées, appeler GetOverlappedResult avec bWait = = FALSe.

**État des thèmes de Shell en mode de contraste élevé**

-   Windows 8 : retourne l’état des thèmes réels pour lorsqu’il est en mode de contraste élevé.
-   Windows 7 : retourne un thème non disponible en mode de contraste élevé, car DWM est toujours activé.
-   Windows Vista (par défaut) : retourne comme non disponible en mode de contraste élevé, car DWM est toujours activé.

**Shell iPersistFile :: Save, méthode**

-   Windows 8 : CShellLink :: Save détermine maintenant si le gestionnaire IPersistFile est appelé avec un argument de chemin d’accès relatif et fait échouer l’appel si c’est le cas.

    La [documentation publique](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) qui décrit ce comportement indique que l’argument de chemin d’accès doit être un chemin d’accès absolu :

-   Windows 7 et versions antérieures (par défaut) : CShellLink :: Save ne détermine pas si le gestionnaire iPersistFile envoie un contrôle de chemin d’accès relatif et permet aux applications de continuer à travailler avec des chemins d’accès absolus ou relatifs.

**Assistant Compatibilité des programmes (PCA)**

-   Windows 8 : les applications avec la section compatibilité n’obtiennent pas l’atténuation de l’APC.
-   Windows 7 : les applications avec la section compatibilité sont suivies pour détecter les problèmes de compatibilité potentiels pour les modifications apportées à Windows 8 (décrits dans ce document).
-   Windows Vista (par défaut) : les applications qui ne parviennent pas à s’installer correctement ou se bloquer pendant l’exécution dans certaines circonstances spécifiques obtiennent l’atténuation de l’APC. Pour plus d’informations, consultez la section ressources.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

Mettez à jour le manifeste d’application avec les dernières informations de compatibilité pour la prise en charge du système d’exploitation. Cette section décrit les ajouts apportés au manifeste :

**Espace de noms :** Compatibility. v1 (xmlns = "urn : schemas-microsoft-com : Compatibility. v1" >)

**Nom de la section :** Compatibilité (nouvelle section)

**Pris en charge :** GUID du système d’exploitation pris en charge : les GUID mappés aux systèmes d’exploitation pris en charge sont les suivants :

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    pour **Windows Vista**: il s’agit de la valeur par défaut pour le contexte Switchback

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    pour **Windows 7**: les applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement de Windows 7

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    pour **Windows 8**: les applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement de Windows 8

Microsoft génère et publie des GUID pour les futures versions de Windows, si nécessaire.

Exemple XML d’un manifeste mis à jour :

> [!Note]  
> L’attribut et les noms de balise dans le manifeste de l’application respectent la casse.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



Les GUID pour tous les systèmes d’exploitation de l’exemple précédent offrent une prise en charge de niveau supérieur. Les applications qui prennent en charge plusieurs plateformes n’ont pas besoin de manifestes séparés pour chaque plateforme.

## <a name="tests"></a>Tests

Une application peut spécifier plusieurs ID de système d’exploitation pris en charge. Vous devez ajouter un ID de système d’exploitation pris en charge si vous avez testé ou si vous êtes en train de tester l’application sur le système d’exploitation. Windows Vista et les versions antérieures du système d’exploitation ne prêtent pas attention à ces entrées. À compter de Windows 7, Windows choisit le GUID de la version la plus élevée dans le manifeste jusqu’à la version Windows en cours d’exécution et donne à ce niveau la prise en charge de l’application. Pour vérifier que l’application fonctionne avec la nouvelle section de compatibilité du manifeste de l’application :

1.  Testez l’application avec la nouvelle section de compatibilité et la prise en charge d’ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} pour vous assurer que l’application fonctionne correctement à l’aide du comportement Windows 8 le plus récent.
2.  Testez l’application avec la nouvelle section de compatibilité et l’ID d’ID pris en charge = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} pour vous assurer que l’application fonctionne correctement à l’aide du comportement de Windows 7.
3.  Testez l’application avec la nouvelle section de compatibilité et l’ID d’ID pris en charge = {e2011457-1546-43C5-a5fe-008deee3d3f0} pour vous assurer que l’application fonctionne correctement à l’aide du comportement de Windows Vista.

## <a name="resources"></a>Ressources

-   [QueryActCtxW fonction)](../sbscs/application-manifests.md)
-   [Manifeste de contrôle de compte d’utilisateur](/previous-versions/bb756929(v=msdn.10))
-   [Manifestes d’application pour les applications Windows](../sbscs/application-manifests.md)
-   [Gestionnaire de fenêtrage (DWM)](../dwm/dwm-overview.md)
-   [Mise à jour des incompatibilités de contexte](https://support.microsoft.com/kb/978637)
-   [Assistant Compatibilité des programmes](/previous-versions/bb756937(v=msdn.10))

 

 