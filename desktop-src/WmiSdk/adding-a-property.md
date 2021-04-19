---
description: Les propriétés des classes WMI décrivent les données relatives à un objet managé.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Ajout d’une propriété WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545087"
---
# <a name="adding-a-wmi-property"></a>Ajout d’une propriété WMI

Les propriétés des classes WMI décrivent les données relatives à un objet managé. Par exemple, **handle**, **ProcessID** et **PageFaults** sont définis en tant que propriétés de la classe de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) et décrivent les aspects d’un processus du système d’exploitation. Pour plus d’informations, consultez [écriture d’un fournisseur de propriétés](writing-a-property-provider.md).

## <a name="defining-a-property-in-mof"></a>Définition d’une propriété dans MOF

Une propriété WMI représente un aspect ou un État dans l’objet. Plutôt que de créer des méthodes qui obtiennent et définissent simplement une valeur, vous pouvez créer une propriété. Par exemple, la propriété **Netactived** de [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) indique si l’état de l’adaptateur est activé ou désactivé. Toutefois, les méthodes [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) et [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) effectuent en fait l’action de modifier l’état de l’adaptateur.

Une propriété doit avoir un type de données. Le type de données du **handle** de propriété du [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) est **String** et le type de données de **PageFaults** est **UInt32**. Si une propriété ne peut avoir que deux États, le type de données de la propriété est normalement défini sur **booléen**.

La propriété peut également être un tableau. Par exemple, la propriété identificateur de sécurité (**sid**) du [**tiers de \_ confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) est un tableau d’octets (**UInt8**) qui contient le SID. Les propriétés peuvent contenir des objets incorporés qui sont des références à une ou plusieurs instances d’une autre classe WMI. La liste de contrôle d’accès discrétionnaire **(DACL)** et les propriétés de liste de contrôle d’accès système **(SACL)** de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), par exemple, sont des tableaux d’objets [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) qui décrivent les groupes et les comptes qui ont accès. La propriété **Group** dans **Win32 \_ SecurityDescriptor** contient une référence à une instance unique de **l' \_ approbation Win32**. Pour plus d’informations, consultez [incorporation d’objets dans une classe](embedded-objects.md).

Une propriété peut avoir plusieurs [*qualificateurs*](gloss-q.md). Ces [qualificateurs](wmi-qualifiers.md) peuvent être [*Common Information Model (CIM)*](gloss-c.md) ou des qualificateurs WMI, ou peuvent être spécifiques à certains types de classes, par exemple, les qualificateurs de la classe de [compteur de performance](qualifiers-specific-to-wmi-performance-classes.md) . Les qualificateurs spécifient un aspect de la propriété, par exemple s’il est en lecture seule ou s’il ne peut pas être modifié sans privilège spécifique. Une application qui tente d’écrire dans la propriété **DACL** [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), par exemple, requiert les privilèges **SeSecurityPrivilege** et **SeRestorePrivilege**. Pour plus d’informations, consultez [Ajout d’un qualificateur](adding-a-qualifier.md).

Enfin, une propriété doit avoir un nom. Vous pouvez nommer une propriété tout cela dans les limites de la pratique de programmation standard. Toutefois, il existe deux exceptions principales. Tout d’abord, vous ne pouvez pas utiliser de mot clé MOF, tel que « Class », comme nom de propriété. Deuxièmement, vous ne pouvez pas utiliser de mots clés WQL, tels que « Group », en tant que nom de propriété. Pour plus d’informations sur les mots clés MOF et WQL, consultez [types de données MOF](mof-data-types.md) et [WQL (SQL pour WMI)](wql-sql-for-wmi.md).

Pour le code C++ et format MOF (MOF), vous déclarez les propriétés d’une classe en même temps que vous déclarez la classe.

**Pour définir une propriété**

-   Incluez le type de données de la propriété, le nom et une valeur par défaut et un qualificateur facultatifs entre les accolades de la description de la classe.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    La classe MyClass de l’exemple précédent a trois propriétés : une chaîne de caractères, un entier signé 32 bits et un entier 32 bits non signé. Un nom ne respectant pas la casse et un type de données MOF sont assignés à chaque propriété.

    Le qualificateur de [**clé**](key-qualifier.md) définit la propriété de type chaîne comme propriété de clé qui identifie de façon unique une instance de la classe. Pour plus d’informations sur les qualificateurs, consultez [Ajout d’un qualificateur](adding-a-qualifier.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une classe](creating-a-class.md)
</dt> </dl>

 

 
