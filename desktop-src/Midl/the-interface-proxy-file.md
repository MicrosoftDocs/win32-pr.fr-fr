---
title: Fichier de proxy d’interface
description: Le fichier de proxy d’interface (U \_ p. c) est un fichier c qui contient des routines équivalentes à celles du stub client et des fichiers stub du serveur d’une interface d’objet (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL et COM MIDL, interfaces, fichiers proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940151"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="3d56e-104">Fichier de proxy d’interface</span><span class="sxs-lookup"><span data-stu-id="3d56e-104">The Interface Proxy File</span></span>

<span data-ttu-id="3d56e-105">Le fichier de proxy d’interface (U \_ p. c) est un fichier c qui contient des routines équivalentes à celles du stub client et des fichiers stub du serveur d’une interface d’objet (com).</span><span class="sxs-lookup"><span data-stu-id="3d56e-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="3d56e-106">Ce fichier contient des implémentations des routines de substitution pour le client et le serveur dans le mode inline du compilateur ou des données équivalentes et des thunks dans les modes interprétés, ainsi que d’autres données de collage COM appropriées, telles que les vtables proxy et stub.</span><span class="sxs-lookup"><span data-stu-id="3d56e-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="3d56e-107">Le fichier proxy d’interface comprend les routines et les données de prise en charge uniquement pour les méthodes des interfaces définies dans le fichier IDL actuel.</span><span class="sxs-lookup"><span data-stu-id="3d56e-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="3d56e-108">Pour clarifier ce comportement, un exemple étendu est utilisé tout au long de cette section.</span><span class="sxs-lookup"><span data-stu-id="3d56e-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="3d56e-109">Lors de la compilation d’un fichier IDL avec une interface telle que IFaceB qui hérite de IFaceA, les données et routines auxiliaires associées à IFaceB sont générées dans le fichier proxy actuel, tandis que l’interface de base IFaceA les données auxiliaires et les routines connexes se trouvent dans le proxy généré à partir du fichier IDL contenant la définition IFaceA.</span><span class="sxs-lookup"><span data-stu-id="3d56e-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="3d56e-110">Le compilateur génère toutes les données nécessaires pour identifier les substituts de l’interface de base et les déléguer quand cela est nécessaire pour prendre en charge les méthodes IFaceA utilisées par le biais de l’interface IFaceB.</span><span class="sxs-lookup"><span data-stu-id="3d56e-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="3d56e-111">Pour chaque méthode d’une interface dans le fichier IDL actuel, le fichier proxy contient les deux méthodes de substitution suivantes lorsqu’elles sont compilées en mode mixte ([/OS](-os.md)), et les données d’interpréteur équivalentes lorsqu’elles sont compilées en mode interpréteur ([/OI](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="3d56e-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="3d56e-112">Le substitut côté client, tel que la \_ méthode IFaceB \_ proxy dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3d56e-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="3d56e-113">Ce substitut côté client est le point d’entrée virtuel sur lequel le client, par exemple IFaceB :: Method, est distribué.</span><span class="sxs-lookup"><span data-stu-id="3d56e-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="3d56e-114">Il marshale les arguments d’entrée dans un formulaire transmissible, transmet les arguments marshalés ainsi que les informations qui identifient l’interface et l’opération, puis démarshale la valeur de retour et tous les arguments de sortie lors du retour de l’opération appelée.</span><span class="sxs-lookup"><span data-stu-id="3d56e-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="3d56e-115">Substitut côté serveur, par exemple, \_ stub de méthode IFaceB \_ .</span><span class="sxs-lookup"><span data-stu-id="3d56e-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="3d56e-116">Ce substitut côté serveur est le point d’entrée virtuel sur lequel le runtime sous-jacent distribue sur le serveur pour émuler le client.</span><span class="sxs-lookup"><span data-stu-id="3d56e-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="3d56e-117">Elle démarshale les arguments d’entrée pour répliquer les données du client, appelle l’implémentation du serveur de la fonction d’interface, puis marshale et transmet la valeur de retour et tous les arguments de sortie au côté client.</span><span class="sxs-lookup"><span data-stu-id="3d56e-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="3d56e-118">Le nom par défaut d’un fichier proxy généré à partir d’un fichier. idl est le fichier \_ p. c. Utilisez le commutateur du compilateur [**/proxy**](-proxy.md) MIDL pour remplacer le nom par défaut du fichier de proxy d’interface.</span><span class="sxs-lookup"><span data-stu-id="3d56e-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="3d56e-119">Les commutateurs [**/env**](-env.md) et [**/out**](-out.md) affectent ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3d56e-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




