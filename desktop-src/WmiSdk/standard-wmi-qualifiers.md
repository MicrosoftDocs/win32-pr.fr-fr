---
description: La liste suivante répertorie les qualificateurs standard spécifiques à WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificateurs WMI standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534619"
---
# <a name="standard-wmi-qualifiers"></a>Qualificateurs WMI standard

La liste suivante répertorie les qualificateurs standard spécifiques à WMI.

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendement**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Indique qu’une classe contient des qualificateurs modifiés qui sont localisés. La valeur par défaut est **true**.

La classe associée peut être traduite. Pour accéder à la version traduite, utilisez l’identificateur de paramètres régionaux pour construire un nom d’espace de noms.

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Ignorer \_ GetObject**
</dt> <dd>

Type de données : **booléen**

S’applique à : méthodes

Indique que l’appel de méthode doit passer directement à l’appel **ExecMethodAsync** du fournisseur plutôt qu’au fournisseur en appelant d’abord un appel à **GetObject** pour valider le chemin d’accès de l’objet. La valeur par défaut est **false**. L’utilisation de la fonction de **contournement \_ GetObject** peut améliorer considérablement les performances.

Avant d’utiliser le **contournement de \_ GetObject**, assurez-vous qu’aucune des actions suivantes n’est effectuée :

-   Dérivez une classe de votre classe.
-   Substituez la méthode qui a le **qualificateur \_ GetObject Bypass** .

L’échec de ces précautions peut entraîner l’appel de l’implémentation de la méthode de la classe parente au lieu de la classe enfant. Pour plus d’informations, consultez Utilisation du \_ qualificateur GetObject de contournement.

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Clé CIM**
</dt> <dd>

Type de données **: \_ valeur booléenne CIM**

S’applique à : Properties

Indique que la propriété associée est une propriété de clé dans CIM, mais pas dans WMI.

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : propriétés, méthodes, paramètres

Contient le texte décrivant le type d’une propriété.

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : classes

Indique qu’une classe a des instances associées à plus d’informations fournies dynamiquement par un fournisseur.

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Déconseillé**
</dt> <dd>

Type de données **: \_ valeur booléenne CIM**

S’applique à : Properties, classes

Indique que la propriété a été remplacée par une autre propriété.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Vidéo**
</dt> <dd>

S’applique à : classes, propriétés

**UUID** de la classe associée.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamique**](dynamic-qualifier.md)
</dt> <dd>

Type de données : **booléen**

S’applique à : classes, propriétés

Indique une classe dont les instances sont créées dynamiquement. La valeur de ce qualificateur doit être définie sur **true**.

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes, instances

Indique qu’une instance de contient des valeurs fournies par les fournisseurs de propriétés dynamiques. La valeur par défaut est **true**.

Vous devez spécifier ce qualificateur sur une telle instance. Seule la valeur **true** est autorisée.

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Des**
</dt> <dd>

Type de données **: \_ valeur booléenne CIM**

S’applique à : instances

Indique que la valeur de cette propriété ne peut pas changer pendant la durée de vie de l’instance.

</dd> <dt>

<span id="ID"></span><span id="id"></span>**IDENTIFI**
</dt> <dd>

Type de données : **VT \_ I4**

S’applique à : propriétés, paramètres

Identifie et séquence de manière unique une propriété ou un paramètre de méthode lorsque les instructions MOF sont générées automatiquement.

Ce qualificateur est requis uniquement pour les paramètres de méthode. Lors de la création de paramètres pour une méthode, les concepteurs de classes doivent commencer par ID (0) pour le premier paramètre et utiliser chaque entier successif pour chaque paramètre successif. Si les qualificateurs d' **ID** ne sont pas intentionnellement omis, le compilateur MOF génère automatiquement des qualificateurs d' **ID** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Été**
</dt> <dd>

Type de données : **booléen**

S’applique à : méthodes

Indique qu’une méthode a une implémentation fournie par un fournisseur.

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : instances

Indique qu’une instance de contient des valeurs fournies par un fournisseur de propriétés dynamiques.

La valeur est passée au fournisseur de propriétés en tant qu’argument de la méthode [**IWbemPropertyProvider :: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Paramètres régionaux**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : classes ou instances

Spécifie la langue d’origine pour une classe ou une instance. Pour plus d’informations sur les valeurs de paramètres régionaux, consultez [codes de paramètres régionaux](#locale-codes).

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : instances d’espace de noms

Spécifie un descripteur de sécurité pour l’espace de noms au format [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md). La chaîne SDDL est traitée par WMI pour établir la sécurité de l’espace de noms, mais elle n’est pas stockée sous forme de chaîne. Si aucun descripteur de sécurité n’est spécifié, la sécurité par défaut est utilisée. Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Facultatif**
</dt> <dd>

Type de données : **booléen**

S’applique à : paramètres

Indique qu’un paramètre n’est pas obligatoire et qu’il a une valeur par défaut avec un comportement correct.

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Autorisations**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : propriétés, méthodes

Ensemble de valeurs utilisées pour informer le client des privilèges requis pour créer des instances, remplir des propriétés ou exécuter des méthodes. La valeur par défaut est **false**.

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : Properties

Indique qu’une propriété d’instance contient des valeurs fournies par les fournisseurs de propriétés dynamiques.

Vous devez spécifier ce qualificateur sur une telle propriété. La valeur est passée au fournisseur de propriétés en tant qu’argument de [**IWbemPropertyProvider :: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : classes

La valeur de ce qualificateur est le nom du fournisseur dynamique qui fournit des instances de classe et actualise les données d’instance. Ce nom doit être inscrit auprès de WMI en créant une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) avec la propriété **Name** contenant ce nom. Quand ce qualificateur est spécifié sur une classe dont les instances sont fournies dynamiquement, le qualificateur **dynamique** doit également être spécifié.

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**
</dt> <dd>

Type de données : **booléen**

S’applique à : instances d’espace de noms

Si la valeur est **true**, **RequiresEncryption** marque un espace de noms afin que les applications et les scripts clients doivent se connecter avec l’authentification chiffrée. Le niveau d’authentification doit être défini sur la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC** en C++. Dans les scripts ou les Visual Basic, le niveau d’authentification doit être défini sur **WbemAuthenticationLevelPktPrivacy**. Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md). Le qualificateur est utilisé dans [*MOF*](gloss-m.md) avec la commande de préprocesseur d’espace de noms pragma.

Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md) ou [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md). Les niveaux d’authentification de script sont définis dans [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

Type de données : **booléen**

S’applique à : classes

Désigne une classe qui ne peut avoir qu’une seule instance et qui ne contient pas de propriétés de clé.

Seule la valeur **true** (valeur par défaut) est autorisée.

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Statique**
</dt> <dd>

Type de données : **booléen**

S’applique à : méthodes

Indique si une méthode peut être appelée à l’aide de la définition de classe ou de ses instances.

La méthode ne peut pas être appelée à partir d’une instance.

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Sous-type**
</dt> <dd>

Type de données : **VT \_ BSTR**

S’applique à : Properties

Indique qu’une propriété de type **\_ DateTime CIM** représente un intervalle de temps plutôt qu’une heure spécifique.

Pour identifier la propriété en tant qu’intervalle, la valeur de ce qualificateur doit être « Interval ». Toutes les autres valeurs de ce qualificateur sont réservées pour une utilisation ultérieure.

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**UNIVERSEL**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes

Identificateur unique universel appliqué à la classe.

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**
</dt> <dd>

Type de données : **chaîne**

S’applique à : classes

Numéro de version de l’objet de classe. La valeur par défaut est **null**. Le numéro de version est incrémenté lorsque des modifications sont apportées à la classe.

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**
</dt> <dd>

Type de données : **tableau de chaînes**

S’applique à : Properties

Ensemble de valeurs indiquant les privilèges système qui doivent être disponibles et activés pour une opération d’écriture réussie.

</dd> </dl>

## <a name="remarks"></a>Notes

### <a name="locale-codes"></a>Codes de paramètres régionaux

Un code de paramètres régionaux se présente sous la forme « MS \_ <Three Digit Language ID> ». Par exemple, les paramètres régionaux anglais sont MS \_ 409. Le tableau suivant répertorie les ID de langue.



| Language              | ID de langue (hexadécimal) |
|-----------------------|---------------------------|
| Arabe                | 401                       |
| Portugais (Brésil)   | 416                       |
| Chinois (simplifié)  | 804                       |
| Chinois (traditionnel) | 404                       |
| Tchèque                 | 405                       |
| Danois                | 406                       |
| Néerlandais                 | 413                       |
| Anglais (par défaut)     | 409                       |
| Finnois               | 40b                       |
| Français                | 40c                       |
| Allemand                | 407                       |
| Grec                 | 408                       |
| Hébreu                | 40d                       |
| Hongrois             | 40e                       |
| Italien               | 410                       |
| Japonais              | 411                       |
| Coréen                | 412                       |
| Norvégien             | 414                       |
| Polonais                | 415                       |
| Portugais (Portugal) | 816                       |
| Russe               | 419                       |
| Espagnol               | c0a                       |
| Suédois               | 41D                       |
| Turc               | 41f                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>Utilisation du \_ qualificateur GetObject Bypass

L’utilisation du qualificateur **\_ GetObject de contournement** sur une méthode peut produire des résultats confuss.

L’exemple suivant définit les classes **Shape** et **Circle** . Notez que la classe **Circle** est dérivée de la classe **Shape** .


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



L’appel suivant à **ExecMethod** utilise un objet **Circle** nommé « MyCircle » pour dessiner un cercle.


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



Dans le scénario précédent, WMI appelle **GetObject**; Découvre que « Shape. Name = 'MyCircle' » est un **cercle**; et exécute l’implémentation de **Circle** de **DrawIt**. Toutefois, si vous utilisez le **qualificateur \_ GetObject du contournement** sur **DrawIt**, WMI n’appelle pas **GetObject**, ne découvre pas que « Shape. Name = 'MyCircle' » est un **cercle** et exécute l’implémentation de **la forme** de **DrawIt** au lieu de l’implémentation de **Circle** de **DrawIt**.

L’appel suivant à **ExecMethod** appelle toujours l’implémentation correcte de **DrawIt**.


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Qualificateurs WMI](wmi-qualifiers.md)
</dt> <dt>

[Ajout d’un qualificateur](adding-a-qualifier.md)
</dt> </dl>

 

