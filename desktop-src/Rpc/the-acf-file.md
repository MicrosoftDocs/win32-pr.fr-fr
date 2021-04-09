---
title: Fichier ACF
description: Le fichier ACF vous permet de personnaliser l’interface RPC de votre client et/ou de vos applications serveur sans affecter les caractéristiques du réseau de l’interface.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941320"
---
# <a name="the-acf-file"></a><span data-ttu-id="1cda3-103">Fichier ACF</span><span class="sxs-lookup"><span data-stu-id="1cda3-103">The ACF File</span></span>

<span data-ttu-id="1cda3-104">Le fichier ACF vous permet de personnaliser l’interface RPC de votre client et/ou de vos applications serveur sans affecter les caractéristiques du réseau de l’interface.</span><span class="sxs-lookup"><span data-stu-id="1cda3-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="1cda3-105">Par exemple, si votre application cliente contient une structure de données complexe qui n’a qu’une signification sur l’ordinateur local, vous pouvez spécifier dans le fichier ACF comment les données de cette structure peuvent être représentées dans un format indépendant de l’ordinateur pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1cda3-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="1cda3-106">Ce didacticiel illustre une autre utilisation du fichier ACF, en spécifiant le type de handle de liaison qui représente la connexion entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="1cda3-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="1cda3-107">L' **\[** [**attribut \_ handle implicite**](/windows/desktop/Midl/implicit-handle) **\]** dans l’en-tête ACF permet à l’application cliente de sélectionner un serveur pour son appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1cda3-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="1cda3-108">Le CCP définit le handle comme étant du handle de [**type \_ t**](/windows/desktop/Midl/handle-t) (un type de données primitif MIDL).</span><span class="sxs-lookup"><span data-stu-id="1cda3-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="1cda3-109">Le compilateur MIDL insère le nom du handle de liaison spécifié par le ACF, Hello \_ IfHandle dans le fichier d’en-tête qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="1cda3-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="1cda3-110">Notez que ce fichier ACF particulier a un corps vide.</span><span class="sxs-lookup"><span data-stu-id="1cda3-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="1cda3-111">Le compilateur MIDL a une option, [**/app \_ config**](/windows/desktop/Midl/-app-config), qui vous permet d’inclure certains attributs ACF, tels **que \_ descripteur implicite**, dans le fichier IDL, plutôt que de créer un fichier ACF distinct.</span><span class="sxs-lookup"><span data-stu-id="1cda3-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="1cda3-112">Envisagez d’utiliser cette option si votre application n’a pas besoin de nombreuses configurations spéciales et si la compatibilité OSF stricte n’est pas un problème.</span><span class="sxs-lookup"><span data-stu-id="1cda3-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 