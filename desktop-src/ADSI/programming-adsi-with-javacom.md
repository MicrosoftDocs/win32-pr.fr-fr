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
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="48488-107">Programmation d’ADSI avec Java/COM</span><span class="sxs-lookup"><span data-stu-id="48488-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="48488-108">À l’aide de la machine virtuelle Microsoft pour Java (machine virtuelle Microsoft) et du compilateur Microsoft Java, vous avez accès à toutes les fonctionnalités ADSI exposées par le biais de tous les composants COM ADSI, à partir d’une application Java/COM.</span><span class="sxs-lookup"><span data-stu-id="48488-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="48488-109">L’exemple de code Java suivant montre les éléments nécessaires à la liaison à un objet ADSI et à l’appel de méthodes sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="48488-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="48488-110">Les fonctions et les méthodes d’objet de l’API ADSI requises sont exposées par le biais de Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="48488-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


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



<span data-ttu-id="48488-111">L’argument de la première instruction **Import** fait référence aux classes wrapper Java empaquetées dans Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="48488-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="48488-112">Utilisez Visual J++ pour créer les classes wrapper et les inclure dans votre projet, en suivant la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="48488-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="48488-113">**Pour créer des classes wrapper et les inclure dans votre projet**</span><span class="sxs-lookup"><span data-stu-id="48488-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="48488-114">Dans un projet Visual J++, sélectionnez **Ajouter un wrapper com...** dans le menu **projet** .</span><span class="sxs-lookup"><span data-stu-id="48488-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="48488-115">Sélectionnez Bibliothèque de types Active Directory dans les **composants installés :** dans la boîte de dialogue wrappers com.</span><span class="sxs-lookup"><span data-stu-id="48488-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="48488-116">Si la bibliothèque de types n’est pas affichée dans la zone de liste, cliquez sur le bouton **Parcourir...** , accédez au répertoire où activeds. tlb est stocké, puis sélectionnez la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="48488-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="48488-117">Visual J++ crée le package activeds pour les classes wrapper Java et inclut le package dans le chemin d’accès par défaut du projet.</span><span class="sxs-lookup"><span data-stu-id="48488-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="48488-118">Pour plus d’informations, consultez le package activeds dans le volet **Explorateur de projets** de la fenêtre Visual J++.</span><span class="sxs-lookup"><span data-stu-id="48488-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="48488-119">Pour obtenir un objet ADSI qui ne peut pas être cocréé, utilisez l’une des fonctions d’API ADSI exposées, par exemple [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), qui sont également empaquetées dans Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="48488-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="48488-120">Microsoft J/direct permet d’accéder à ces API et à d’autres API natives.</span><span class="sxs-lookup"><span data-stu-id="48488-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="48488-121">Cela est illustré par les deux dernières lignes de l’exemple de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="48488-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="48488-122">Lors de la compilation, assurez-vous que l’option Microsoft Language extension est activée.</span><span class="sxs-lookup"><span data-stu-id="48488-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="48488-123">Pour ce faire, sélectionnez **<project> Propriétés...** dans le menu **projet** de la fenêtre de projet Visual J++.</span><span class="sxs-lookup"><span data-stu-id="48488-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="48488-124">Ensuite, cliquez sur l’onglet **compiler** dans la boîte de dialogue **<project> Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="48488-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="48488-125">Désactivez la case à cocher **Désactiver les extensions de langage Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="48488-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="48488-126">Si vous compilez à partir de la ligne de commande, utilisez le commutateur « /x- », par exemple :</span><span class="sxs-lookup"><span data-stu-id="48488-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="48488-127">**JVC/x-SimpleADSI. Java**</span><span class="sxs-lookup"><span data-stu-id="48488-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="48488-128">Enfin, pour que l’ordinateur virtuel charge le composant COM, la bibliothèque de liens dynamiques (DLL) doit être visible sur le chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="48488-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="48488-129">Si une erreur « Java. lang. UnsatisfiedLinkError » est retournée, définissez le chemin d’accès pour inclure le chemin d’accès qui contient la DLL requise.</span><span class="sxs-lookup"><span data-stu-id="48488-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="48488-130">Par exemple, si Activeds.dll a été installé dans c : \\ ADSI \\ lib, émettez la commande suivante à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="48488-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="48488-131">**définir le chemin d’accès =% PATH%; c : \\ bibliothèque ADSI ADSI \\**</span><span class="sxs-lookup"><span data-stu-id="48488-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




