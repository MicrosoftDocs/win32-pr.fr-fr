---
title: Restauration des objets supprimés
description: Windows Server 2003 comprend les objets \ 0034 ; Restore Deleted Objects \ 0034 ; fonctionnalité.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Restauration des objets supprimés
- Active Directory, utiliser, restaurer des objets supprimés
- objets AD, restauration des objets supprimés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104507858"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="27241-106">Restauration des objets supprimés</span><span class="sxs-lookup"><span data-stu-id="27241-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="27241-107">Windows Server 2003 comprend la fonctionnalité « restaurer les objets supprimés ».</span><span class="sxs-lookup"><span data-stu-id="27241-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="27241-108">Pour activer la restauration d’objets supprimés, au moins un contrôleur de domaine du domaine doit s’exécuter sur Windows Server 2003 ou une version ultérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="27241-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="27241-109">Par défaut, seuls les administrateurs de domaine peuvent restaurer des objets supprimés, même si cela peut être délégué à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="27241-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="27241-110">Les limitations suivantes s’appliquent à la restauration d’objets supprimés :</span><span class="sxs-lookup"><span data-stu-id="27241-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="27241-111">Impossible de restaurer un objet lorsque la durée de vie de désactivation de l’objet a expiré car, lorsque la durée de vie de la désactivation a expiré, l’objet est supprimé définitivement.</span><span class="sxs-lookup"><span data-stu-id="27241-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="27241-112">Les objets qui existent à la racine du contexte d’appellation, tels qu’une partition de domaine ou d’application, ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="27241-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="27241-113">Les objets de schéma ne peuvent pas être restaurés.</span><span class="sxs-lookup"><span data-stu-id="27241-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="27241-114">Les objets de schéma ne doivent jamais être supprimés.</span><span class="sxs-lookup"><span data-stu-id="27241-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="27241-115">Il est possible de restaurer les conteneurs supprimés, mais la restauration des objets supprimés qui se trouvaient dans le conteneur avant la suppression est difficile, car l’arborescence sous le conteneur doit être reconstruite manuellement.</span><span class="sxs-lookup"><span data-stu-id="27241-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="27241-116">Autorisations nécessaires pour restaurer un objet supprimé</span><span class="sxs-lookup"><span data-stu-id="27241-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="27241-117">Lorsqu’un objet est supprimé, le descripteur de sécurité de l’objet est conservé.</span><span class="sxs-lookup"><span data-stu-id="27241-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="27241-118">Bien que le propriétaire soit identifiable à partir du descripteur de sécurité, pour des raisons de sécurité, seuls les administrateurs de domaine sont autorisés à restaurer des objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="27241-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="27241-119">Les administrateurs de domaine peuvent accorder l’autorisation de restaurer des objets de suppression à d’autres utilisateurs et groupes en accordant à l’utilisateur ou au groupe le droit d’accès du contrôle « réanimer tombstone ».</span><span class="sxs-lookup"><span data-stu-id="27241-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="27241-120">Le droit d’accès du contrôle de réanimation tombstone est accordé à la racine du contexte d’appellation.</span><span class="sxs-lookup"><span data-stu-id="27241-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="27241-121">Seuls les utilisateurs disposant d’une autorisation d’accès en lecture sur un objet et ses attributs sont autorisés à lire l’objet et les attributs accessibles une fois l’objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="27241-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="27241-122">L’octroi à un utilisateur de cette autorisation peut être un risque pour la sécurité, car il peut permettre à l’utilisateur de restaurer un objet de compte qui a accès aux ressources auxquelles l’utilisateur n’a normalement pas accès.</span><span class="sxs-lookup"><span data-stu-id="27241-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="27241-123">En restaurant un compte, l’utilisateur gagne le contrôle de ce compte, car il doit définir le mot de passe initial sur le compte lorsque le compte est restauré.</span><span class="sxs-lookup"><span data-stu-id="27241-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="27241-124">Pour restaurer complètement un objet supprimé, l’utilisateur doit :</span><span class="sxs-lookup"><span data-stu-id="27241-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="27241-125">Avoir, ou être membre d’un groupe qui a, le droit d’accès du contrôle « réanimer les objets tombstone ».</span><span class="sxs-lookup"><span data-stu-id="27241-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="27241-126">Avoir un accès en écriture pour chaque attribut obligatoire nécessitant une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="27241-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="27241-127">Avoir un accès en écriture au nom unique relatif (RDN).</span><span class="sxs-lookup"><span data-stu-id="27241-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="27241-128">Avoir un accès en écriture à chaque attribut facultatif qui doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="27241-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="27241-129">Avoir des droits de création d’enfants sur le conteneur de destination pour la classe d’objet de l’objet restauré.</span><span class="sxs-lookup"><span data-stu-id="27241-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="27241-130">L’attribut **IsDeleted** n’est pas vérifié au cours de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="27241-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="27241-131">Aucune des autorisations supprimer-enfant sur le conteneur « objets supprimés » n’est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="27241-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="27241-132">Restauration d’un objet supprimé</span><span class="sxs-lookup"><span data-stu-id="27241-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="27241-133">Pour restaurer un objet supprimé, l’objet doit d’abord se trouver dans le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="27241-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="27241-134">Pour plus d’informations sur la récupération des objets supprimés, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="27241-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="27241-135">Lorsque l’objet a été localisé, les opérations suivantes doivent être effectuées dans une seule opération LDAP.</span><span class="sxs-lookup"><span data-stu-id="27241-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="27241-136">Pour cela, vous devez utiliser la fonction [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) avec le contrôle [**\_ \_ Show \_ Deleted \_ OID du serveur LDAP**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .</span><span class="sxs-lookup"><span data-stu-id="27241-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="27241-137">Supprimez la valeur de l’attribut **IsDeleted** .</span><span class="sxs-lookup"><span data-stu-id="27241-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="27241-138">La valeur de l’attribut **IsDeleted** doit être supprimée, et non définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="27241-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="27241-139">Remplacez le nom unique de l’objet pour qu’il soit déplacé vers un conteneur autre que le conteneur objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="27241-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="27241-140">Il peut s’agir de n’importe quel conteneur qui peut normalement contenir l’objet.</span><span class="sxs-lookup"><span data-stu-id="27241-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="27241-141">Le nom unique du conteneur précédent de l’objet se trouve dans l’attribut **lastKnownParent** de l’objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="27241-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="27241-142">L’attribut **lastKnownParent** est défini uniquement si l’objet a été supprimé sur un contrôleur de domaine Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="27241-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="27241-143">Par conséquent, il est possible que le contenu de l’attribut **lastKnownParent** ne soit pas exact.</span><span class="sxs-lookup"><span data-stu-id="27241-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="27241-144">Restaurez les attributs obligatoires pour l’objet qui ont été effacés pendant la suppression.</span><span class="sxs-lookup"><span data-stu-id="27241-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="27241-145">L’attribut **objectCategory** peut également être défini lors de la restauration de l’objet, mais il n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="27241-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="27241-146">Si aucune valeur **objectCategory** n’est spécifiée, le **objectCategory** par défaut de l' **objectClass** de l’objet est utilisé.</span><span class="sxs-lookup"><span data-stu-id="27241-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="27241-147">Une fois l’objet restauré, il est accessible tel qu’il était avant sa suppression.</span><span class="sxs-lookup"><span data-stu-id="27241-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="27241-148">À ce stade, tous les attributs facultatifs qui sont importants doivent être restaurés.</span><span class="sxs-lookup"><span data-stu-id="27241-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="27241-149">Toutes les références à l’objet à partir d’autres objets dans le répertoire doivent également être restaurées.</span><span class="sxs-lookup"><span data-stu-id="27241-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="27241-150">Comme mesure de sécurité, les objets utilisateur sont désactivés lorsqu’ils sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="27241-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="27241-151">Les objets utilisateur doivent être activés après la restauration des attributs facultatifs pour permettre l’utilisation de l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27241-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="27241-152">Pour plus d’informations et pour obtenir un exemple de code qui montre comment restaurer un objet supprimé, reportez-vous à la fonction RestoreDeletedObject ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="27241-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="27241-153">RestoreDeletedObject</span><span class="sxs-lookup"><span data-stu-id="27241-153">RestoreDeletedObject</span></span>

<span data-ttu-id="27241-154">L’exemple de code C++ suivant montre comment restaurer un objet supprimé.</span><span class="sxs-lookup"><span data-stu-id="27241-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 