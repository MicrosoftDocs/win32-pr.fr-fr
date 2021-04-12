---
title: Authentification (ADSI)
description: Dans ADSI, les informations d’identification qui se composent d’un nom d’utilisateur et d’un mot de passe sont utilisées pour fournir ou restreindre l’accès aux objets dans le service d’annuaire.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- Authentification ADSI
- ADSI, utilisation, authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462723"
---
# <a name="authentication-adsi"></a><span data-ttu-id="fca75-105">Authentification (ADSI)</span><span class="sxs-lookup"><span data-stu-id="fca75-105">Authentication (ADSI)</span></span>

<span data-ttu-id="fca75-106">Dans ADSI, les informations d’identification qui se composent d’un nom d’utilisateur et d’un mot de passe sont utilisées pour fournir ou restreindre l’accès aux objets dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fca75-106">In ADSI, credentials that consist of a user name and password are used to provide or restrict access to objects in the directory service.</span></span> <span data-ttu-id="fca75-107">La fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) utilise les informations d’identification du thread appelant pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="fca75-107">The [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function uses the credentials of the calling thread for authentication.</span></span> <span data-ttu-id="fca75-108">La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) peuvent être utilisées pour spécifier des informations d’identification autres que celles du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="fca75-108">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method can be used to specify credentials other than those of the calling thread.</span></span> <span data-ttu-id="fca75-109">Lorsqu’un objet est lié à avec un utilisateur authentifié, l’utilisateur est autorisé à accéder à l’objet tel qu’il est pris en charge par les exigences de sécurité du service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fca75-109">When an object is bound to with an authenticated user, the user is allowed access to the object as supported by the underlying directory service security requirements.</span></span>

> [!Note]  
> <span data-ttu-id="fca75-110">La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ne doivent pas être utilisées pour valider les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fca75-110">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method should not be used to validate user credentials.</span></span> <span data-ttu-id="fca75-111">Pour plus d’informations sur la validation des informations d’identification de l’utilisateur, consultez l’article 180548 de la base de connaissances Microsoft [Comment : valider les informations d’identification de l’utilisateur sur les systèmes d’exploitation Microsoft](https://support.microsoft.com/kb/180548).</span><span class="sxs-lookup"><span data-stu-id="fca75-111">For more information about validating user credentials, see Microsoft Knowledge Base article 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).</span></span>

 

<span data-ttu-id="fca75-112">L’exemple de code suivant montre comment utiliser la méthode [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) pour authentifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fca75-112">The following code example shows how to use the [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method to authenticate a user.</span></span>


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




