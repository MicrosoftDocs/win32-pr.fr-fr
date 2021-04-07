---
title: ADsPath de Winnt
description: Cette rubrique contient des exemples de chaînes à utiliser pour la valeur ADsPath de Winnt.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Fournisseur de services Winnt ADSI, Winnt ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939566"
---
# <a name="winnt-adspath"></a><span data-ttu-id="9749d-105">ADsPath de Winnt</span><span class="sxs-lookup"><span data-stu-id="9749d-105">WinNT ADsPath</span></span>

<span data-ttu-id="9749d-106">La chaîne ADsPath du fournisseur ADSI Winnt peut prendre l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9749d-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="9749d-107">Le nom de domaine peut être un nom NETBIOS ou un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="9749d-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="9749d-108">Le serveur est le nom d’un serveur spécifique dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="9749d-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="9749d-109">Le chemin d’accès correspond au chemin d’accès de l’objet, tel que « printserver1/exemple ».</span><span class="sxs-lookup"><span data-stu-id="9749d-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="9749d-110">Le nom de l’objet est le nom d’un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="9749d-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="9749d-111">La classe d’objet est le nom de classe de l’objet nommé.</span><span class="sxs-lookup"><span data-stu-id="9749d-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="9749d-112">Voici un exemple de cette utilisation : « WinNT://MyServer/JeffSmith,user ».</span><span class="sxs-lookup"><span data-stu-id="9749d-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="9749d-113">La spécification d’un nom de classe peut améliorer les performances de l’opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="9749d-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




