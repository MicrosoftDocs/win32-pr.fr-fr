---
description: Définit le descripteur de sécurité pour l’espace de noms auquel un utilisateur est connecté. Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Méthode configured de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 04da59b6370e2e9a381f2e3889b75ac37cb926e54c46cc0e616ec5353ed6f665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132032"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Méthode configured de la \_ \_ classe SystemSecurity

La méthode **configured** définit le descripteur de sécurité pour l’espace de noms auquel un utilisateur est connecté. Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) . Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).

Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide de [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Un utilisateur doit disposer de l’autorisation **Write \_ DAC** et, par défaut, un administrateur dispose de cette autorisation. La seule partie du descripteur de sécurité utilisée est l’entrée de contrôle d’accès (ACE) non héritée dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). En définissant l’indicateur **conteneur d' \_ héritage** dans les ACE, le descripteur de sécurité affecte les espaces de noms enfants. Les ACE allow et Deny sont autorisées.

> [!Note]  
> Étant donné que les ACE Deny et allow sont toutes deux autorisées dans une liste DACL, l’ordre des ACE est important. Pour plus d’informations, consultez [classement des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Syntaxe


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SD* \[ dans\]
</dt> <dd>

Tableau d’octets qui compose le descripteur de sécurité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un **HRESULT** qui indique l’état d’un appel de méthode. pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [parameters. ReturnValue](parsing-outparameters-objects.md). Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

La liste suivante répertorie les valeurs de retour qui sont significatives pour les **paramètres**.

<dl> <dt>

**\_OK**
</dt> <dd>

Méthode exécutée avec succès.

</dd> <dt>

**\_accès WBEM \_ E \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des droits suffisants pour appeler cette méthode.

</dd> <dt>

**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd>

Tentative d’exécution de cette méthode sur le système d’exploitation qui ne la prend pas en charge.

</dd> <dt>

**WBEM \_ E \_ objet non valide \_**
</dt> <dd>

SD ne passe pas les tests de validité de base.

</dd> <dt>

**\_paramètre WBEM E \_ non valide \_**
</dt> <dd>

SD n’est pas valide en raison de l’un des éléments suivants :

-   DACL est manquant.
-   DACL n’est pas valide.
-   L’entrée de contrôle d’accès est associée à l’indicateur **WBEM \_ Full \_ Write \_ REP** et l’indicateur **WBEM écriture \_ partielle \_ \_ WBEM** ou **\_ \_ fournisseur d’écriture WBEM** n’est pas défini.
-   L’entrée du contrôle d’accès a l’indicateur **\_ \_ ACE inherit only** défini sans l’indicateur **\_ \_ ACE inherit du conteneur** .
-   L’ACE a un jeu de bits d’accès inconnu.
-   L’ACE a un indicateur défini qui ne figure pas dans la table.
-   Le type de l’entrée du contrôle d’accès n’est pas dans la table.
-   Le propriétaire et le groupe sont absents du SD.

Pour plus d’informations sur les indicateurs d’entrée de contrôle d’accès (ACE), consultez [constantes de sécurité WMI](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la modification de la sécurité des espaces de noms par programmation ou manuelle, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Exemples

Le script suivant montre comment utiliser SETD pour définir le descripteur **de sécurité** de l’espace de noms pour l’espace de noms racine et le remplacer par le tableau d’octets affiché dans *strSD*.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



L’exemple de code C# suivant utilise System. Security. AccessControl. RawSecurityDescriptor pour énumérer, insérer et supprimer de nouveaux objets CommonAce dans RawSecurityDescriptor. DiscretionaryAcl, puis le reconvertir en tableau d’octets pour l’enregistrer via le paramètre. Un SecurityIdentifier peut être récupéré à l’aide de NTAccount et de translate.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity :: est**](--systemsecurity-getsd.md)
</dt> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

