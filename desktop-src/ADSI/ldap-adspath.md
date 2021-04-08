---
title: Chemin d’authentification LDAP
description: Cette rubrique montre la syntaxe que vous devez utiliser pour l’ADsPath LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- Chemin d’authentification LDAP
- ADsPath, LDAP, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730308"
---
# <a name="ldap-adspath"></a><span data-ttu-id="311b9-105">Chemin d’authentification LDAP</span><span class="sxs-lookup"><span data-stu-id="311b9-105">LDAP ADsPath</span></span>

<span data-ttu-id="311b9-106">Le chemin ADsPath du fournisseur LDAP Microsoft requiert le format suivant.</span><span class="sxs-lookup"><span data-stu-id="311b9-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="311b9-107">Les crochets gauche et droit ( \[ \] ) indiquent des paramètres facultatifs ; il ne s’agit pas d’une partie littérale de la chaîne de liaison.</span><span class="sxs-lookup"><span data-stu-id="311b9-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="311b9-108">Le « nom d’hôte » peut être un nom d’ordinateur, une adresse IP ou un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="311b9-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="311b9-109">Un nom de serveur peut également être spécifié dans la chaîne de liaison.</span><span class="sxs-lookup"><span data-stu-id="311b9-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="311b9-110">La plupart des fournisseurs LDAP suivent un modèle qui requiert la spécification d’un nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="311b9-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="311b9-111">Le « numéro_port » spécifie le port à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="311b9-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="311b9-112">Si aucun numéro de port n’est spécifié, le fournisseur LDAP utilise le numéro de port par défaut.</span><span class="sxs-lookup"><span data-stu-id="311b9-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="311b9-113">Le numéro de port par défaut est 389 si vous n’utilisez pas de connexion SSL ou 636 si vous utilisez une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="311b9-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="311b9-114">Le « DistinguishedName » spécifie le nom unique d’un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="311b9-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="311b9-115">Un nom unique pour un objet donné est garanti être unique.</span><span class="sxs-lookup"><span data-stu-id="311b9-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="311b9-116">Le tableau suivant répertorie des exemples de chaînes de liaison.</span><span class="sxs-lookup"><span data-stu-id="311b9-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="311b9-117">Exemple d’ADsPath LDAP</span><span class="sxs-lookup"><span data-stu-id="311b9-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="311b9-118">Description</span><span class="sxs-lookup"><span data-stu-id="311b9-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="311b9-119">LDAP</span><span class="sxs-lookup"><span data-stu-id="311b9-119">LDAP:</span></span>                                                     | <span data-ttu-id="311b9-120">Liez à la racine de l’espace de noms LDAP.</span><span class="sxs-lookup"><span data-stu-id="311b9-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="311b9-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="311b9-121">LDAP://server01</span></span>                                           | <span data-ttu-id="311b9-122">Effectuer une liaison à un serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="311b9-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="311b9-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="311b9-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="311b9-124">Établit une liaison à un serveur spécifique en utilisant le numéro de port spécifié.</span><span class="sxs-lookup"><span data-stu-id="311b9-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="311b9-125">LDAP : 0408 = Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="311b9-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="311b9-126">Lier à un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="311b9-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="311b9-127">LDAP://server01/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="311b9-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="311b9-128">Effectuer une liaison à un objet spécifique par le biais d’un serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="311b9-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="311b9-129">Si l’authentification Kerberos est requise pour la réussite d’une demande de répertoire spécifique, la chaîne de liaison doit utiliser soit un ADsPath sans serveur, tel que LDAP : menée = Jeff Smith, CN = Users, DC = fabrikam, DC = com, soit un ADsPath avec un nom de serveur DNS complet, par exemple LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="311b9-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="311b9-130">La liaison au serveur à l’aide d’un nom NETBIOS plat ou d’un nom DNS courts, par exemple, en utilisant le nom SERVEUR01 au lieu de server01.fabrikam.com, n’est pas garantie d’obtenir l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="311b9-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="311b9-131">Pour plus d’informations et pour obtenir des exemples de chaînes de liaison LDAP, ainsi qu’une description des caractères spéciaux qui peuvent être utilisés dans les chaînes de liaison LDAP, consultez l’ADsPath LDAP.</span><span class="sxs-lookup"><span data-stu-id="311b9-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="311b9-132">**Windows 2000 avec SP1 et versions ultérieures :** Avec le fournisseur LDAP, si une chaîne de liaison comprend un nom de serveur, vous pouvez augmenter les performances en utilisant l’indicateur de **\_ \_ liaison de serveur ADS** avec la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="311b9-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="311b9-133">L’indicateur de **\_ \_ liaison de serveur ADS** indique qu’un nom de serveur a été spécifié, ce qui permet à ADSI d’éviter un trafic réseau supplémentaire et inutile.</span><span class="sxs-lookup"><span data-stu-id="311b9-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="311b9-134">Caractères spéciaux LDAP</span><span class="sxs-lookup"><span data-stu-id="311b9-134">LDAP Special Characters</span></span>

<span data-ttu-id="311b9-135">LDAP a plusieurs caractères spéciaux qui sont réservés à une utilisation par l’API LDAP.</span><span class="sxs-lookup"><span data-stu-id="311b9-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="311b9-136">La liste des caractères spéciaux se trouve dans [noms uniques](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="311b9-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="311b9-137">Pour utiliser l’un de ces caractères dans un ADsPath sans générer d’erreur, le caractère doit être précédé d’une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="311b9-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="311b9-138">C’est ce que l’on appelle le caractère d' *échappement* .</span><span class="sxs-lookup"><span data-stu-id="311b9-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="311b9-139">Par exemple, si un nom d’utilisateur est fourni sous la forme " <last name> , <first name> ", la virgule de la valeur de nom doit être placée dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="311b9-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="311b9-140">La chaîne obtenue ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="311b9-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="311b9-141">Le caractère d’échappement peut également être spécifié par son code hexadécimal à deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="311b9-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="311b9-142">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="311b9-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="311b9-143">Les caractères non imprimables, tels que le saut de ligne et le retour chariot, doivent être placés dans une séquence d’échappement et spécifiés par leur code hexadécimal à deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="311b9-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="311b9-144">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="311b9-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="311b9-145">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="311b9-145">For More Information</span></span>

<span data-ttu-id="311b9-146">Pour plus d’informations sur la notation de nom unique utilisée par les services d’annuaire compatibles LDAP, consultez [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="311b9-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 