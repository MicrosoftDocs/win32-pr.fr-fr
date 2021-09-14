---
description: En général, chaque objet Active Directory est mappé à une seule instance WMI.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Mappage d’instances Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51eaec7b2c6ef121d0f65df375e1bb0fce32cc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918799"
---
# <a name="mapping-active-directory-instances"></a>Mappage d’instances Active Directory

En général, chaque objet Active Directory est mappé à une seule instance WMI. La classe WMI qui correspond à l’instance WMI est la même que la classe fournie par le fournisseur de classe de la classe de Active Directory correspondante. La propriété de clé **ADSIPath** de chaque instance est renseignée avec le chemin d’accès ADSI de l’objet.

Les sections suivantes sont présentées dans cette rubrique :

-   [Mapper des espaces de noms](#mapping-namespaces)
-   [Mappage des valeurs d’attribut](#mapping-attribute-values)
-   [Mappage des associations d’instances](#mapping-instance-associations)

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Mapper des espaces de noms

Chacun des espaces de noms dans ADSI est mappé un-à-un vers les espaces de noms de l' \\ espace de noms du répertoire racine WMI \\ . Le nom de l’espace de noms WMI est le même que la valeur **ProgID** du fournisseur de services d’annuaire qui fournit l’espace de noms. Plus précisément, Active Directory est mappé à l' \\ espace de noms LDAP dans l' \\ espace de noms du répertoire racine \\ . WMI crée l' \\ espace de noms LDAP dans le cadre du processus d’inscription du fournisseur de classe.

## <a name="mapping-attribute-values"></a>Mappage des valeurs d’attribut

Le tableau suivant répertorie le mappage entre chaque attribut d’un objet Active Directory et une propriété WMI.



| Syntaxe de Active Directory | Type de données WMI                                 | Valeur de la propriété WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Booléen                 | **\_valeur BOOLÉENNE CIM**                              | Mappé directement à la valeur booléenne appropriée.                         |
| Chaîne non sensible à la casse | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Chaîne respectant la casse   | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Nom unique      | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| DN-Binary               | Objet incorporé de classe **DN \_ avec \_ binaire** | Mappé aux instances du **DN avec la \_ classe \_ String** .                    |
| DN-String               | Objet incorporé de la classe **DN \_ avec \_ String** | Mappé aux instances du **DN avec la \_ classe \_ String** .                    |
| Énumération             | **\_SINT32 CIM**                               | Mappé directement à la valeur entière.                                     |
| IA5-String              | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Integer                 | **\_SINT32 CIM**                               | Mappé directement à la valeur entière.                                     |
| Descripteur de sécurité NT  | Objet incorporé de la classe **Uint8Array**       | Mappé aux instances de la classe **Uint8Array** .                          |
| Chaîne numérique          | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| ID objet               | **\_chaîne CIM**                               | Mappé à partir de la représentation sous forme de chaîne de l’OID ; par exemple, « 1.3.3.4 ». |
| Chaîne d’octets            | Objet incorporé de la classe **Uint8Array**       | Mappé aux instances de la classe **Uint8Array** .                          |
| OU le nom                 | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Presentation-Address    | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Imprimer la chaîne de cas       | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Lien de réplica            | Objet incorporé de la classe **Uint8Array**       | Mappé aux instances de la classe **Uint8Array** .                          |
| SID                     | Objet incorporé de la classe **Uint8Array**       | Mappé aux instances de la classe **Uint8Array** .                          |
| Temps                    | **\_DateTime CIM**                             | Converti en représentation de \_ DateTime CIM et mappé.                 |
| Indéfini               | N/A                                           | N/A                                                                       |
| Chaîne Unicode          | **\_chaîne CIM**                               | Mappé à partir de la valeur de la chaîne.                                      |
| Heure du code UTC          | **\_DateTime CIM**                             | Converti en représentation de \_ DateTime CIM et mappé.                 |



 

Pour plus d’informations sur **Uint8Array** et **DN \_ avec \_ binaire**, consultez [mappage d’attributs](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Mappage des associations d’instances

Le fournisseur de services d’annuaire mappe les différentes relations de conteneur dans Active Directory à l’aide d’instances de la classe de [**\_ \_ \_ relation contenant-contenu de l’instance DS LDAP**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) .

 

 
