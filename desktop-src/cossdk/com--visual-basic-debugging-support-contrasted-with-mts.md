---
description: Prise en charge du débogage des Visual Basic COM+ avec MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Prise en charge du débogage des Visual Basic COM+ avec MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513942"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Prise en charge du débogage des Visual Basic COM+ avec MTS

COM+ supprime ou réduit plusieurs limites du débogage avec Microsoft Visual Basic 6,0 et MTS. La liste suivante récapitule les modifications que vous pouvez attendre avec COM+ :

-   Débogage de plusieurs composants : dans COM+, vous pouvez déboguer des scénarios dans lesquels un client s’exécutant dans une instance de l’IDE effectue des appels à n’importe quel nombre de dll s’exécutant dans un autre en tant que groupe de projets. Les objets dans les projets de DLL groupés peuvent se composer les uns les autres arbitrairement, en passant le contexte en fonction des besoins. Bien entendu, cela fonctionne également lorsque les dll et le client se trouvent dans le même groupe de projets dans la même instance de l’IDE.

-   Limitations du débogage pour \_ les événements Class Initialize et Class \_ Terminate : avec com+, vous pouvez placer du code dans les \_ événements Class Initialize et Class \_ Terminate d’un composant d’application com+ même si ce code tente d’accéder à l’objet ou à son objet de contexte correspondant. Vous pouvez définir des points d’arrêt à cet emplacement et utiliser des montres. Vous pouvez également définir des points d’arrêt dans l’événement de fin de classe \_ .

    Bien qu’il ne soit plus nécessaire comme solution de contournement, vous pouvez toujours implémenter l’interface [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) et utiliser ses méthodes [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) et [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) si vous devez exécuter du code au démarrage et à l’arrêt de votre composant. Vous pouvez également placer des points d’arrêt dans le code pour les méthodes **Deactivate** ou [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) .

-   La surveillance des objets MTS : avec COM+, vous pouvez ajouter des espions pour les variables d’objet retournées par COM+, y compris les valeurs de retour des méthodes [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)et [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) .

-   Stabilité accrue lorsque les composants échouent : dans COM+, l’échec d’un composant ne s’arrête toujours pas Visual Basic (qui s’exécute dans le même processus que le composant débogué). Par exemple, la prise en charge des échecs de réactivation juste-à-temps (JIT) vous permet désormais d’examiner le contexte de l’objet pendant le débogage.

-   Le débogueur peut réactiver les objets publiés par COM+ : comme avec MTS, Visual Basic 6,0 peut réactiver les objets COM+ pendant que vous déboguez une seule étape via un client. En raison de la façon dont Visual Basic 6,0 Découvre des informations sur les objets, il s’agit d’un comportement attendu. Considérons par exemple le code suivant :

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Si le obj. La méthode de test appelle [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), com+ libère immédiatement obj de la mémoire, mais obj n’a pas encore été défini sur Nothing. Quand obj. Le test retourne, le débogueur Visual Basic appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur obj pour l’interface [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) . Le wrapper de contexte associé à obj crée une nouvelle instance de MyApp. MyClass pour traiter l’appel **QueryInterface** . En conséquence, vous verrez cet objet non initialisé dans le débogueur après obj. Le test a été retourné. Cet objet apparaît uniquement dans le débogueur et est supprimé par l’instruction suivante pour affecter à obj la valeur Nothing.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Débogage dans l’IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
