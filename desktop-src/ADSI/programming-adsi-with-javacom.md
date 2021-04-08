---
title: Programmation d’ADSI avec Java/COM
description: À l’aide de la machine virtuelle Microsoft pour Java (machine virtuelle Microsoft) et du compilateur Microsoft Java, vous avez accès à toutes les fonctionnalités ADSI exposées par le biais de tous les composants COM ADSI, à partir d’une application Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmation d’ADSI avec Java/COM AD
- ADSI ADSI, utilisation de, programmation Java/COM pour
- ADSI ADSI, exemple de code Java
- ADSI ADSI, exemple de code Java, liaison à un objet ADSI et appel de méthodes sur cet objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839150"
---
# <a name="programming-adsi-with-javacom"></a>Programmation d’ADSI avec Java/COM

À l’aide de la machine virtuelle Microsoft pour Java (machine virtuelle Microsoft) et du compilateur Microsoft Java, vous avez accès à toutes les fonctionnalités ADSI exposées par le biais de tous les composants COM ADSI, à partir d’une application Java/COM. L’exemple de code Java suivant montre les éléments nécessaires à la liaison à un objet ADSI et à l’appel de méthodes sur cet objet. Les fonctions et les méthodes d’objet de l’API ADSI requises sont exposées par le biais de Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



L’argument de la première instruction **Import** fait référence aux classes wrapper Java empaquetées dans Activeds.dll. Utilisez Visual J++ pour créer les classes wrapper et les inclure dans votre projet, en suivant la procédure ci-dessous.

**Pour créer des classes wrapper et les inclure dans votre projet**

1.  Dans un projet Visual J++, sélectionnez **Ajouter un wrapper com...** dans le menu **projet** .
2.  Sélectionnez Bibliothèque de types Active Directory dans les **composants installés :** dans la boîte de dialogue wrappers com. Si la bibliothèque de types n’est pas affichée dans la zone de liste, cliquez sur le bouton **Parcourir...** , accédez au répertoire où activeds. tlb est stocké, puis sélectionnez la bibliothèque de types.

Visual J++ crée le package activeds pour les classes wrapper Java et inclut le package dans le chemin d’accès par défaut du projet. Pour plus d’informations, consultez le package activeds dans le volet **Explorateur de projets** de la fenêtre Visual J++.

Pour obtenir un objet ADSI qui ne peut pas être cocréé, utilisez l’une des fonctions d’API ADSI exposées, par exemple [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), qui sont également empaquetées dans Activeds.dll. Microsoft J/direct permet d’accéder à ces API et à d’autres API natives. Cela est illustré par les deux dernières lignes de l’exemple de code ci-dessus.

Lors de la compilation, assurez-vous que l’option Microsoft Language extension est activée. Pour ce faire, sélectionnez **<project> Propriétés...** dans le menu **projet** de la fenêtre de projet Visual J++. Ensuite, cliquez sur l’onglet **compiler** dans la boîte de dialogue **<project> Propriétés** . Désactivez la case à cocher **Désactiver les extensions de langage Microsoft** . Si vous compilez à partir de la ligne de commande, utilisez le commutateur « /x- », par exemple :

**JVC/x-SimpleADSI. Java**

Enfin, pour que l’ordinateur virtuel charge le composant COM, la bibliothèque de liens dynamiques (DLL) doit être visible sur le chemin d’accès système. Si une erreur « Java. lang. UnsatisfiedLinkError » est retournée, définissez le chemin d’accès pour inclure le chemin d’accès qui contient la DLL requise. Par exemple, si Activeds.dll a été installé dans c : \\ ADSI \\ lib, émettez la commande suivante à partir de la ligne de commande :

**définir le chemin d’accès =% PATH%; c : \\ bibliothèque ADSI ADSI \\**

 

 




