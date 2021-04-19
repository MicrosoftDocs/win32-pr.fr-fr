---
description: WMI possède plusieurs objets d’assistance de script qui fournissent les conversions requises par les scripts.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Objets d’assistance de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545807"
---
# <a name="scripting-helper-objects"></a>Objets d’assistance de script

WMI possède plusieurs objets d’assistance de script qui fournissent les conversions requises par les scripts.

Les objets d’assistance de script WMI sont les suivants :

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**\_SecurityDescriptorHelper Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Les objets d’assistance décomposent les structures de données composites afin qu’un script ne soit pas requis pour analyser la structure afin d’obtenir l’un des éléments. Par exemple, la structure **DateTime WMI** ne peut pas être affichée directement et est différente des autres structures de données Windows DateTime, telles que **VT \_ Date**.

## <a name="swbemdatetime"></a>SWbemDateTime

L’objet [**SWbemDateTime**](swbemdatetime.md) fournit des propriétés qui analysent le jour, le mois, l’année, l’heure de la journée, et ainsi de suite. Il fournit également des méthodes de conversion pour convertir la valeur DateTime de Windows Management Instrumentation (WMI) vers et à partir des formats de **\_ Date** et [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) VT. Pour les paramètres de sécurité Internet Explorer (IE), l’objet **SWbemDateTime** est le seul objet de script WMI marqué comme sécurisé pour l’initialisation et sécurisé pour les scripts. Pour obtenir plus d’informations et des exemples de conversions de date et d’heure, consultez [dates et heures](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) et l’article sur technet scriptcenter [il s’agit du temps (OH et des dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="swbemobjectpath"></a>SWbemObjectPath

Les propriétés de [**SWbemObjectPath**](swbemobjectpath.md) fournissent le chemin d’accès absolu d’un objet, mais découpent également les parties du chemin d’accès WMI, telles que le serveur, l’espace de noms, la classe ou le chemin d’accès relatif. L’objet vous permet de définir la sécurité du chemin d’accès, d’obtenir les valeurs de clé des objets représentant le chemin d’accès, de déterminer si un objet est un singleton, et ainsi de suite. Pour plus d’informations sur l’utilisation des chemins d’accès aux objets WMI, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>\_SecurityDescriptorHelper Win32

La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) convertit le descripteur de sécurité d’un objet sécurisable d’un format à un autre.

De nombreux objets, tels que les imprimantes, les espaces de noms WMI, les clés de registre ou les applications DCOM, ont des descripteurs de sécurité qui contrôlent l’accès à l’objet. Vous pouvez utiliser WMI pour découvrir ou modifier qui a accès à ces objets en obtenant ou en définissant le descripteur de sécurité associé à l’objet.

Toutefois, différentes méthodes peuvent obtenir des descripteurs de sécurité dans un tableau d’octets binaire, le format SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) ) ou en tant qu’instance de [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). La forme de tableau d’octets binaire d’un descripteur de sécurité ne doit pas être manipulée, sauf par les méthodes C++ conçues pour les [opérations de descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-operations). Les descripteurs dans le langage SDDL sont dans des chaînes, mais ils sont toujours difficiles à manipuler. Le format le plus simple à manipuler est **Win32 \_ SecurityDescriptor**, car il contient des objets incorporés pour le tiers de confiance, l’ACE et le SID. Pour plus d’informations sur la structure des descripteurs de sécurité dans WMI, consultez [objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md). Pour plus d’informations sur la façon d’effectuer des conversions, consultez [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
