---
description: Windows wmi (management instrumentation) est l’infrastructure de données et d’opérations de gestion sur les systèmes d’exploitation basés sur Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows Management Instrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b08c0301881b57c8132be9eead2e5b52cb64d4d3c4278985a573d5bff94f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553133"
---
# <a name="windows-management-instrumentation"></a>Windows Management Instrumentation

## <a name="purpose"></a>Fonction

Windows wmi (management instrumentation) est l’infrastructure de données et d’opérations de gestion sur les systèmes d’exploitation basés sur Windows. vous pouvez écrire des scripts ou des applications wmi pour automatiser des tâches administratives sur des ordinateurs distants, mais WMI fournit également des données de gestion à d’autres parties du système d’exploitation et des produits, par exemple System Center Operations Manager, anciennement Microsoft Operations Manager (MOM) ou Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).

> [!Note]  
> La documentation suivante est destinée aux développeurs et aux administrateurs informatiques. Si vous êtes un utilisateur final qui a rencontré un message d’erreur concernant WMI, vous devez accéder à [support Microsoft](https://support.microsoft.com/) et rechercher le code d’erreur que vous voyez dans le message d’erreur. Pour plus d’informations sur la résolution des problèmes liés aux scripts WMI et au service WMI, consultez [WMI ne fonctionne pas.](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

> [!Note]  
> WMI est entièrement pris en charge par Microsoft ; toutefois, la version la plus récente des scripts et du contrôle d’administration est disponible par le biais de l’Infrastructure de gestion Windows (MI). MI est entièrement compatible avec les versions précédentes de WMI et fournit un hôte de fonctionnalités et d’avantages qui facilitent la conception et le développement de fournisseurs et de clients. pour plus d’informations, consultez [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).

 

## <a name="where-applicable"></a>Le cas échéant

WMI peut être utilisé dans toutes les applications basées sur Windows, et est particulièrement utile dans les applications d’entreprise et les scripts d’administration.

Les administrateurs système peuvent trouver des informations sur l’utilisation de WMI dans le [scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)TechNet et dans divers ouvrages sur WMI. Pour plus d’informations, consultez [informations supplémentaires](further-information.md).

## <a name="developer-audience"></a>Développeurs concernés

WMI est conçu pour les programmeurs qui utilisent C/C++, l’application microsoft Visual Basic, ou un langage de script qui a un moteur sur Windows et gère les objets microsoft ActiveX. Bien qu’une certaine connaissance de la programmation COM soit utile, les développeurs C++ qui écrivent des applications peuvent trouver de bons exemples pour commencer à [créer une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md).

pour développer des fournisseurs de code managé ou des applications en C# ou Visual Basic .net à l’aide du .NET Framework, consultez [WMI dans .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

De nombreux administrateurs et professionnels de l’informatique accèdent à WMI via PowerShell. L’applet de commande obtenir-WMI pour PowerShell vous permet de récupérer des informations pour un référentiel WMI local ou distant. Par conséquent, plusieurs rubriques et classes, en particulier dans la section [création de clients WMI](creating-wmi-clients.md) , contiennent des exemples PowerShell. pour plus d’informations sur l’utilisation de PowerShell, consultez [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) et l' [écriture de scripts avec Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur le système d’exploitation requis pour utiliser un élément d’API spécifique ou une classe WMI, consultez la section relative à la configuration requise de chaque rubrique dans la documentation WMI.

Si un composant attendu semble manquer, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

Vous n’avez pas besoin de télécharger ou d’installer un kit de développement logiciel (SDK) spécifique pour créer des scripts ou des applications pour WMI. Toutefois, certains outils d’administration WMI sont utiles aux développeurs. Pour plus d’informations, consultez la section téléchargements dans [informations supplémentaires](further-information.md).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dd>

Informations générales sur WMI.

</dd> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> <dd>

Informations sur le développement d’applications pour utiliser WMI, qui comprend des informations sur les outils.

</dd> <dt>

[Référence WMI](wmi-reference.md)
</dt> <dd>

Documentation relative aux classes WMI, aux classes WMI C++, à l’API COM WMI, à l’API de script et à d’autres documents de référence WMI.

</dd> </dl>

 

 
