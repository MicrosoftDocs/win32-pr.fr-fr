---
description: Fournit des règles pour le mappage des classes WMI à Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapper des classes Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992899"
---
# <a name="mapping-active-directory-classes"></a>Mapper des classes Active Directory

Étant donné que Active Directory possède un large éventail d’objets possibles, WMI ne peut pas créer un mappage direct un-à-un. Au lieu de cela, le fournisseur de services d’annuaire utilise des règles pour mapper les classes entre les deux technologies.

Les sections suivantes sont abordées dans cette rubrique :

-   [Mapper des classes](#mapping-classes)
-   [Mappage d’attributs](#mapping-attributes)
-   [Classes d’association](#association-classes)

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Mapper des classes

La liste suivante décrit les instructions utilisées par le fournisseur de services d’annuaire pour mapper des classes Active Directory à des classes WMI :

-   Chaque classe abstraite du schéma Active Directory est mappée à une classe abstraite dans le schéma WMI.

    Dans le schéma WMI, chaque classe abstraite est précédée de DS \_ . Par exemple, la classe **Person** du schéma Active Directory est mappée à la classe WMI Person de la **\_ personne** .

-   Chaque classe non abstraite du schéma Active Directory est mappée aux deux classes suivantes dans le schéma WMI :

    -   La première classe mappée est précédée de publicités \_ . Il s’agit de classes abstraites, mappées selon les règles ci-dessous.
    -   La deuxième classe mappée est une classe non abstraite avec le préfixe de nom de service d’annuaire \_ . Cette classe est dérivée de la \_ classe abstraite ADS, avec l’ajout du qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) .

    Par exemple, la classe **utilisateur** du schéma Active Directory est mappée à deux classes. La première classe est la classe abstraite **\_ utilisateur ADS** , mappée selon les règles ci-dessous. La deuxième classe est la classe non abstraite de l' **\_ utilisateur DS** . Elle est dérivée de l' **\_ utilisateur ADS** et a le qualificateur de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) ajouté.

-   Sauf spécification contraire, le nom d’une classe mappée est la valeur tronquée de la propriété **LDAP-Display-Name** dans la classe Active Directory.
-   Si la propriété **sous-classe-de** est présente dans la classe Active Directory, la classe mappée WMI est dérivée de la classe spécifiée.

    Si la propriété **de sous-classe** n’est pas présente, la classe mappée WMI est dérivée de la classe de la **\_ \_ \_ classe racine LDAP DS** , comme indiqué dans le fichier MOF.

    > [!Note]  
    > Cette classe possède la propriété de clé **ADSIPath** , avec un type **VT \_ BSTR**. Il s’agit du chemin d’accès ADSI unique qui identifie cette instance. Active Directory prend en charge uniquement l’héritage unique, ce qui fonctionne.

     

-   Un qualificateur **dynamique** de type **VT \_ bool** et Flavor ayant la valeur `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **true** est créé pour chaque classe. Il s’agit d’un qualificateur WMI standard qui indique que les instances de cette classe sont fournies dynamiquement.
-   Si la classe n’est pas abstraite, le fournisseur crée un qualificateur de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) de type **VT \_ BSTR bool** et qualificateur Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` défini sur « fournisseur d’instance DS » pour chaque classe. Il s’agit d’un qualificateur WMI standard qui indique le nom du fournisseur qui fournit dynamiquement des instances de cette classe.

Le reste des propriétés ADSI est mappé aux qualificateurs et aux propriétés de classe, conformément aux tableaux suivants. Tous les qualificateurs sont mappés avec une valeur d’indicateur de qualificateur de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

La liste suivante répertorie les informations de mappage pour la classe Active Directory, en présentant le qualificateur WMI et le type de qualificateur WMI pour chaque propriété Active Directory.

<dl> <dt>

**Nom commun**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Mappé directement à partir de la valeur de chaîne.

</dd> <dt>

**Default-Object-catégorie**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Mappé directement à partir de la valeur de chaîne.

</dd> <dt>

**Descripteur de sécurité par défaut**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Mappé directement à partir de la valeur de chaîne.

</dd> <dt>

**Régit l’ID**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Mappé à partir de la représentation sous forme de chaîne de l’OID ; par exemple, « {1 3 3 6} ».

</dd> <dt>

**Classe d’objet**
</dt> <dd>

N/A

Non mappé.

</dd> <dt>

**Catégorie objet-classe**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Mappé directement à partir de la valeur entière. En outre, si la valeur est abstract (2), le qualificateur standard **VT \_ bool** CIM, appelé qualificateur **« abstract »** , est également créé.

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Mappé à partir de la représentation sous forme de chaîne de la valeur OID ; par exemple, « {1 3 3 6} ». En outre, la propriété identifiée ici est annotée avec le qualificateur CIM **indexé** standard défini sur **true**.

</dd> <dt>

**Système uniquement**
</dt> <dd>

**SystemOnly** (**VT \_ bool**)

Mappé directement à partir de la valeur booléenne.

</dd> </dl>

 

La liste suivante répertorie les propriétés de la classe Active Directory mappées aux propriétés de la classe WMI.

<dl> <dt>

**Peut contenir**
</dt> <dd>

Chaque propriété de cette liste est mappée à une propriété WMI.

</dd> <dt>

**Doit contenir**
</dt> <dd>

Chaque propriété de cette liste est mappée à une propriété WMI. Le qualificateur CIM standard **not \_ null** est créé pour chacun d’entre eux.

</dd> <dt>

**Système-peut contenir**
</dt> <dd>

Chaque propriété de cette liste est mappée à une propriété WMI. En outre, chaque propriété est annotée avec un qualificateur **système** , défini sur **true**.

</dd> <dt>

**Système-doit contenir**
</dt> <dd>

Chaque propriété de cette liste est mappée à une propriété WMI. Le qualificateur CIM standard **not \_ null** est créé pour chacun d’entre eux. En outre, chaque propriété est annotée avec un qualificateur **système** , défini sur **true**.

</dd> </dl>

## <a name="mapping-attributes"></a>Mappage d’attributs

Le fournisseur de services d’annuaire mappe chaque attribut d’une classe Active Directory à une seule propriété de la classe WMI correspondante, conformément aux règles de cette section. En général, le fournisseur de services d’annuaire nomme la propriété WMI en tant que version tronquée de la valeur **LDAP-Display-Name** de l’attribut Active Directory.

Si la propriété Active Directory **est définie sur une** **valeur** unique, la propriété WMI est combinée avec l’opérateur ou avec un **tableau d' \_ indicateurs \_ CIM**. Notez que chaque propriété est marquée avec le qualificateur **VT \_ BSTR** , **ADSyntax**. Il représente la syntaxe de Active Directory sous-jacente.

Le tableau suivant répertorie le mappage de la syntaxe de Active Directory au type de données de la propriété WMI.



| Élément Active Directory                                      | Type de données WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Point d’accès**](/windows/desktop/ADSchema/s-object-access-point)            | **\_chaîne CIM**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **\_valeur BOOLÉENNE CIM**                                                        |
| **Chaîne non sensible à la casse**                                   | **\_chaîne CIM**                                                         |
| [**Chaîne respectant la casse**](/windows/desktop/ADSchema/s-string-case-sensitive) | **\_chaîne CIM**                                                         |
| [**Nom unique**](/windows/desktop/ADSchema/s-object-ds-dn)             | **\_chaîne CIM**                                                         |
| [**DN-binaire**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Objet incorporé de la classe **DN \_ avec le \_ binaire** défini ci-dessous.<br/> |
| [**DN-chaîne**](/windows/desktop/ADSchema/s-object-dn-string)                  | Objet incorporé de la classe **DN \_ avec la \_ chaîne** définie ci-dessous.<br/> |
| [**Énumération**](/windows/desktop/ADSchema/s-enumeration)                     | **\_SINT32 CIM**                                                         |
| [**Énumération**](/windows/desktop/ADSchema/s-enumeration)                     | **\_chaîne CIM**                                                         |
| [**Entier**](/windows/desktop/ADSchema/s-integer)                             | **\_SINT32 CIM**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **\_chaîne CIM**                                                         |
| Descripteur de sécurité                                           | Objet incorporé de la classe **Uint8Array** défini ci-dessous.<br/>       |
| Chaîne numérique                                                | **\_chaîne CIM**                                                         |
| ID objet                                                     | **\_chaîne CIM**                                                         |
| Chaîne d’octets                                                  | Objet incorporé de la classe **Uint8Array** défini ci-dessous.<br/>       |
| OU le nom                                                       | **\_chaîne CIM**                                                         |
| Presentation-Address                                          | Objet incorporé de la classe **Uint8Array** défini ci-dessous.<br/>       |
| Imprimer la chaîne de cas                                             | **\_chaîne CIM**                                                         |
| Lien de réplica                                                  | Objet incorporé de la classe **Uint8Array** défini ci-dessous.<br/>       |
| [**Chaîne (SID)**](/windows/desktop/ADSchema/s-string-sid)                      | Objet incorporé de la classe **Uint8Array** défini ci-dessous.<br/>       |
| Temps                                                          | **\_DateTime CIM**                                                       |
| Heure du code UTC                                                | **\_DateTime CIM**                                                       |
| Chaîne Unicode                                                | **\_chaîne CIM**                                                         |



 

La syntaxe de la chaîne d’octets, qui fait référence à un tableau de valeurs **UInt8** , pose un problème lorsqu’elle est mappée à WMI, car WMI autorise des propriétés de types **UInt8** et des tableaux de **uint8**, tandis que Active Directory autorise des propriétés de type chaîne d’octets, ainsi que des tableaux de chaîne d’octets.

L’exemple suivant illustre la classe de fournisseur de services d’annuaire utilisée pour mapper un tableau de propriétés de type chaîne d’octets.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI mappe toutes les chaînes d’octets Active Directory les valeurs de propriété aux instances incorporées de **Uint8Array**. De même, WMI mappe des tableaux de chaînes d’octets à des tableaux d’objets **Uint8Array** incorporés.

L’exemple suivant montre les classes qui sont mappées par WMI à DN-Binary et DN-String valeurs de propriété de service d’annuaire.

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

Le tableau suivant répertorie comment WMI mappe le reste des propriétés d’interface d’attribut Active Directory aux qualificateurs de propriété WMI.



| Attribut Active Directory-nom de propriété | Qualificateur WMI       | Type de données    | Informations de mappage                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Syntaxe d’attribut**                     | **AttributeSyntax** | **VT \_ BSTR** | Mappé à partir de la représentation sous forme de chaîne de l’OID. |
| **Nom commun**                          | **CN**              | **VT \_ BSTR** | Mappé à partir de la valeur de chaîne.                     |
| **Système uniquement**                          | **Système**          | **VT \_ bool** | Mappé à partir de la valeur booléenne.                    |



 

> [!Note]  
> WMI mappe tous les qualificateurs de Active Directory avec les `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` versions de qualificateur.

 

## <a name="association-classes"></a>Classes d’association

Le service d’annuaire est essentiellement un magasin hiérarchique d’objets. Les objets qui peuvent apparaître à un niveau non-feuille dans la hiérarchie sont appelés « conteneurs ». La structure de cette hiérarchie est contrôlée par les propriétés « Poss-Superior » et « System-Poss-Superiors » d’une classe dans le schéma. Ceux-ci, pris ensemble, spécifient le jeu de classes dont les instances peuvent être contenues dans une instance d’une classe de conteneur.

L’exemple suivant modélise une association CIM en tant qu’instances de la classe d’association statique [**\_ \_ \_ relation contenant-contenu de la classe LDAP DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

Le fournisseur de classes d’association prend en charge les méthodes [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) et [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .

 

