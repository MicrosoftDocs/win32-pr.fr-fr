---
description: Manifeste d’application
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifeste d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ea81440458bb5ac106fd891cc370ebb2b2fcc1db2a70022bf746bd81dd1acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680209"
---
# <a name="application-manifest"></a>Manifeste d’application

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Windows 7 introduit une nouvelle section dans le manifeste de l’application appelée « compatibilité ». cette section vous aide à Windows déterminer les versions de Windows qu’une application a été conçue pour cibler, et permet à Windows de fournir le comportement attendu par l’application en fonction de la version de Windows ciblée par l’application.

la section compatibilité permet à Windows de fournir un nouveau comportement aux nouveaux logiciels créés par des développeurs tout en conservant la compatibilité des logiciels existants. cette section vous aide également à Windows offrir une meilleure compatibilité dans les futures versions de Windows. par exemple, une application qui déclare uniquement la prise en charge de Windows 7 dans la section compatibilité continuera à recevoir le comportement Windows 7 dans la prochaine version de Windows.

## <a name="manifestation-of-change"></a>Manifeste de modification

les Applications sans section de compatibilité dans leur manifeste recevront Windows comportement de Vista par défaut sur Windows 7 et versions ultérieures Windows. notez que Windows XP et Windows Vista ignorent cette section du manifeste et qu’il n’a aucun impact sur ceux-ci.

les composants de Windows suivants fournissent un comportement divergent en fonction de la section compatibilité dans Windows 7 :

**Pool de threads par défaut RPC**

-   **Windows 7 :** Pour améliorer l’évolutivité et réduire le nombre de threads, RPC bascule vers le pool de threads NT (pool par défaut). pour Windows Vista, RPC utilisait un pool de threads privés.
    -   Pour les fichiers binaires compilés pour Win7, le pool par défaut est utilisé
    -   Si I \_ RpcMgmtEnableDedicatedThreadPool est appelé avant l’appel d’une API RPC, le pool de threads privés est utilisé (comportement Vista)
    -   Si j' \_ RpcMgmtEnableDedicatedThreadPool est appelé après un appel RPC, le pool par défaut est utilisé, je \_ RpcMgmtEnableDedicatedThreadPool renvoie l’erreur 1764 et l’opération demandée n’est pas prise en charge
-   **Windows Vista (par défaut) :** pour les fichiers binaires compilés pour Windows Vista et versions antérieures, le pool privé est utilisé.

**Verrouillage DirectDraw**

-   **Windows 7 :** les Applications manifestées pour Windows 7 ne peuvent pas appeler l’API lock dans DDRAW pour verrouiller la mémoire tampon de la vidéo principale du bureau. Cela génère une erreur et le renvoi du pointeur **null** pour le réplica principal est retourné. Ce comportement est appliqué même si Gestionnaire de fenêtrage composition n’est pas activée. les applications compatibles Windows 7 ne doivent pas verrouiller la mémoire tampon vidéo principale à restituer.
-   **Windows Vista (par défaut) :** Les applications seront en mesure d’acquérir un verrou sur la mémoire tampon vidéo principale, car les applications héritées dépendent de ce comportement. L’exécution de l’application désactive Gestionnaire de fenêtrage.

**Transfert de bloc binaire (BLT) DirectDraw vers le réplica principal sans fenêtre de détourage**

-   **Windows 7 :** les Applications manifestées pour Windows 7 ne sont pas en mesure d’exécuter des Blt sur la mémoire tampon vidéo principale du bureau sans fenêtre de détourage. Cela génère une erreur et la zone BLT ne s’affiche pas. Windows applique ce comportement même si vous n’activez pas la Composition Gestionnaire de fenêtrage. les applications compatibles Windows 7 doivent être Blt dans une fenêtre de détourage.
-   **Windows Vista (par défaut) :** Les applications doivent pouvoir accéder au BLT sur le réplica principal sans fenêtre de découpage, car les applications héritées dépendent de ce comportement. L’exécution de cette application désactive l’Gestionnaire de fenêtrage.

**API GetOverlappedResult**

-   **Windows 7 :** Résout une condition de concurrence où une application multithread utilisant GetOverlappedResult peut retourner sans réinitialiser l’événement dans la structure OVERLAPPED, provoquant le retour prématuré de l’appel suivant à cette fonction.
-   **Windows Vista (par défaut) :** Fournit le comportement avec la condition de concurrence sur laquelle les applications peuvent avoir une dépendance. les Applications qui souhaitent éviter cette concurrence avant le comportement Windows 7 doivent attendre l’événement overlapped et, lorsqu’elles sont signalées, appeler GetOverlappedResult avec bWait = = **false**.

**Assistant Compatibilité des programmes (PCA)**

-   **Windows 7 :** La section applications avec compatibilité n’obtiendra pas l’atténuation de l’APC.
-   **Windows Vista (par défaut) :** Les applications qui ne parviennent pas à s’installer correctement ou se bloquer lors de l’exécution dans certaines circonstances spécifiques obtiennent l’atténuation de l’APC. Pour plus d’informations, consultez la section référence.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

Mettez à jour le manifeste d’application avec les dernières informations de compatibilité pour la prise en charge du système d’exploitation. La section décrit les ajouts au manifeste :

-   **Espace de noms :** Compatibility. v1 (xmlns = "urn : schemas-microsoft-com : Compatibility. v1" >)

-   **Nom de la section :** Compatibilité (nouvelle section)

-   **Pris en charge :** GUID du système d’exploitation pris en charge : les GUID mappés aux systèmes d’exploitation pris en charge sont les suivants :

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} pour Windows Vista : il s’agit de la valeur par défaut pour le contexte switchback.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} pour Windows 7 : les Applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement Windows 7.

    > [!Note]  
    > Microsoft génère et publie des guid pour les futures versions de Windows en fonction des besoins.

     

Voici un exemple de manifeste mis à jour.

> [!Note]  
> L’attribut et les noms de balise dans le manifeste de l’application respectent la casse.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



La valeur de l’ajout de GUID pour les deux systèmes d’exploitation dans l’exemple ci-dessus consiste à fournir une prise en charge de niveau supérieur. Les applications qui prennent en charge les deux plateformes n’ont pas besoin de manifestes séparés pour chaque plateforme.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

1.  testez l’application avec la nouvelle section de compatibilité et `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` assurez-vous que l’application fonctionne correctement à l’aide du dernier comportement de Windows 7
2.  testez l’application avec la nouvelle section de compatibilité et `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (ou sans cette section) pour vous assurer que l’application fonctionne correctement à l’aide des comportements Windows Vista sur Windows 7

## <a name="known-issues"></a>Problèmes connus

**Incompatibilité de contexte** une application s’exécute dans un contexte Windows Vista au lieu d’un contexte Windows 7 sur un ordinateur qui exécute une édition x64 de Windows 7 ou Windows Server 2008 R2.

**Solution** des mises à jour sont disponibles pour corriger cette erreur pour toutes les versions x64 prises en charge de Windows 7 et Windows server 2008 r2, ainsi que pour toutes les versions Itanium prises en charge de Windows Server 2008 r2. accédez à la page de Support Microsoft pour [KB 978637 : une application s’exécute dans un contexte Windows Vista plutôt que dans un contexte Windows 7 sur un ordinateur qui exécute une édition x64 de Windows 7 ou Windows Server 2008 R2](https://support.microsoft.com/kb/978637) pour obtenir des détails supplémentaires et télécharger la version appropriée pour votre système.

**Diagnostic de vidage sur incident bloqué**

**Solution** accédez à la page de Support Microsoft pour [KB 976038 : les Exceptions levées à partir d’une application qui s’exécute dans une version 64 bits de Windows sont ignorées](https://support.microsoft.com/kb/976038) pour obtenir des détails supplémentaires.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [**QueryActCtxW fonction)**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifeste de contrôle de compte d’utilisateur](/previous-versions/bb756929(v=msdn.10))
-   [manifestes d’Application pour les applications Windows](../sbscs/application-manifests.md)
-   [Gestionnaire de fenêtrage (DWM)](../dwm/dwm-overview.md)
-   [Mise à jour des incompatibilités de contexte](https://support.microsoft.com/kb/978637)

 

 
