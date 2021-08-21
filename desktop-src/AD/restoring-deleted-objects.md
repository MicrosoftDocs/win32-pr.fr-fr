---
title: Restauration des objets supprimés
description: Windows Le serveur 2003 comprend les objets \ 0034 ; Restore Deleted Objects \ 0034 ; fonctionnalité.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Restauration des objets supprimés
- Active Directory, utiliser, restaurer des objets supprimés
- objets AD, restauration des objets supprimés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431bcddcbd15366a6accf9b8368fa8d34377b27af923fb102803b6316462634e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025117"
---
# <a name="restoring-deleted-objects"></a>Restauration des objets supprimés

Windows Le serveur 2003 comprend la fonctionnalité « restaurer les objets supprimés ».

pour activer la restauration d’objets supprimés, au moins un contrôleur de domaine dans le domaine doit être en cours d’exécution sur Windows Server 2003 ou une version ultérieure de Windows. Par défaut, seuls les administrateurs de domaine peuvent restaurer des objets supprimés, même si cela peut être délégué à d’autres utilisateurs.

Les limitations suivantes s’appliquent à la restauration d’objets supprimés :

-   Impossible de restaurer un objet lorsque la durée de vie de désactivation de l’objet a expiré car, lorsque la durée de vie de la désactivation a expiré, l’objet est supprimé définitivement.
-   Les objets qui existent à la racine du contexte d’appellation, tels qu’une partition de domaine ou d’application, ne peuvent pas être restaurés.
-   Les objets de schéma ne peuvent pas être restaurés. Les objets de schéma ne doivent jamais être supprimés.
-   Il est possible de restaurer les conteneurs supprimés, mais la restauration des objets supprimés qui se trouvaient dans le conteneur avant la suppression est difficile, car l’arborescence sous le conteneur doit être reconstruite manuellement.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Autorisations nécessaires pour restaurer un objet supprimé

Lorsqu’un objet est supprimé, le descripteur de sécurité de l’objet est conservé. Bien que le propriétaire soit identifiable à partir du descripteur de sécurité, pour des raisons de sécurité, seuls les administrateurs de domaine sont autorisés à restaurer des objets supprimés. Les administrateurs de domaine peuvent accorder l’autorisation de restaurer des objets de suppression à d’autres utilisateurs et groupes en accordant à l’utilisateur ou au groupe le droit d’accès du contrôle « réanimer tombstone ». Le droit d’accès du contrôle de réanimation tombstone est accordé à la racine du contexte d’appellation. Seuls les utilisateurs disposant d’une autorisation d’accès en lecture sur un objet et ses attributs sont autorisés à lire l’objet et les attributs accessibles une fois l’objet supprimé.

> [!Note]  
> L’octroi à un utilisateur de cette autorisation peut être un risque pour la sécurité, car il peut permettre à l’utilisateur de restaurer un objet de compte qui a accès aux ressources auxquelles l’utilisateur n’a normalement pas accès. En restaurant un compte, l’utilisateur gagne le contrôle de ce compte, car il doit définir le mot de passe initial sur le compte lorsque le compte est restauré.

 

Pour restaurer complètement un objet supprimé, l’utilisateur doit :

-   Avoir, ou être membre d’un groupe qui a, le droit d’accès du contrôle « réanimer les objets tombstone ».

-   Avoir un accès en écriture pour chaque attribut obligatoire nécessitant une mise à jour.

-   Avoir un accès en écriture au nom unique relatif (RDN).

-   Avoir un accès en écriture à chaque attribut facultatif qui doit être mis à jour.

-   Avoir des droits de création d’enfants sur le conteneur de destination pour la classe d’objet de l’objet restauré.

    > [!Note]  
    > L’attribut **IsDeleted** n’est pas vérifié au cours de l’opération de restauration. Aucune des autorisations supprimer-enfant sur le conteneur « objets supprimés » n’est vérifiée.

     

## <a name="restoring-a-deleted-object"></a>Restauration d’un objet supprimé

Pour restaurer un objet supprimé, l’objet doit d’abord se trouver dans le conteneur objets supprimés. Pour plus d’informations sur la récupération des objets supprimés, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).

Lorsque l’objet a été localisé, les opérations suivantes doivent être effectuées dans une seule opération LDAP. Pour cela, vous devez utiliser la fonction [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) avec le contrôle [**\_ \_ Show \_ Deleted \_ OID du serveur LDAP**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .

-   Supprimez la valeur de l’attribut **IsDeleted** . La valeur de l’attribut **IsDeleted** doit être supprimée, et non définie sur **false**.
-   Remplacez le nom unique de l’objet pour qu’il soit déplacé vers un conteneur autre que le conteneur objets supprimés. Il peut s’agir de n’importe quel conteneur qui peut normalement contenir l’objet. Le nom unique du conteneur précédent de l’objet se trouve dans l’attribut **lastKnownParent** de l’objet supprimé. l’attribut **lastKnownParent** est défini uniquement si l’objet a été supprimé sur un contrôleur de domaine Windows Server 2003. Par conséquent, il est possible que le contenu de l’attribut **lastKnownParent** ne soit pas exact.
-   Restaurez les attributs obligatoires pour l’objet qui ont été effacés pendant la suppression.

> [!Note]  
> L’attribut **objectCategory** peut également être défini lors de la restauration de l’objet, mais il n’est pas obligatoire. Si aucune valeur **objectCategory** n’est spécifiée, le **objectCategory** par défaut de l' **objectClass** de l’objet est utilisé.

 

Une fois l’objet restauré, il est accessible tel qu’il était avant sa suppression. À ce stade, tous les attributs facultatifs qui sont importants doivent être restaurés. Toutes les références à l’objet à partir d’autres objets dans le répertoire doivent également être restaurées.

Comme mesure de sécurité, les objets utilisateur sont désactivés lorsqu’ils sont restaurés. Les objets utilisateur doivent être activés après la restauration des attributs facultatifs pour permettre l’utilisation de l’objet utilisateur.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment restaurer un objet supprimé, reportez-vous à la fonction RestoreDeletedObject ci-dessous.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

L’exemple de code C++ suivant montre comment restaurer un objet supprimé.


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



 

 