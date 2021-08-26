---
title: .NET Framework les paramètres par défaut
description: .NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b45aef294e035f5fb7e647c49b22206ac8aadd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883122"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif

## <a name="platforms"></a>Plateformes

**Clients** Windows 8     
**serveurs** Windows Server 2012     

## <a name="description"></a>Description

.NET Framework 4,5 est activé par défaut dans Windows 8. Windows 8 n’inclut pas .net 3,5 par défaut, mais les fichiers pour .net 3,5 sont disponibles sur le support d’installation Windows 8 en tant que fonctionnalité facultative.

si l’utilisateur met à niveau Windows 7 vers Windows 8, .NET Framework 3,5 est entièrement activé pour s’assurer que toutes les applications sur l’ordinateur continuent de fonctionner correctement.

## <a name="manifestation"></a>Manifestation

si l’utilisateur effectue une nouvelle installation de Windows 8, puis installe les applications qui requièrent .NET Framework 3,5 (ou 2,0), il déclenchera une demande pour les fichiers .net 3,5 nécessaires. normalement, les fichiers manquants seront téléchargés à partir de Windows Update (après avoir demandé l’autorisation à l’utilisateur), mais si l’accès à Windows Update n’est pas possible, l’activation de .NET Framework 3,5 échouera, sauf si une autre source pour les fichiers manquants a été spécifiée.

## <a name="mitigation"></a>Limitation des risques

pour activer .NET Framework 3,5 sur les ordinateurs de test uniquement avec des installations propres de Windows 8 :

1.  Copiez \\ \\ les sources côte \\ à côte de l’image ISO de la build du système d’exploitation monté vers dotnet35 ou un dossier similaire. Par exemple :
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Exécutez cette ligne de commande en utilisant des privilèges d’administrateur :
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> Le dossier de sources \\ SxS ne doit pas être utilisé comme mécanisme de redistribution, car il ne s’agit pas d’un mécanisme pris en charge.



## <a name="solution"></a>Solution

**Pour les consommateurs :**

Windows 8 comprend un mécanisme qui active automatiquement .NET Framework 3,5 lors de la tentative d’installation du package redistribuable ou lorsqu’un programme d’installation d’application nécessitant .net 3,5 appelle le package redistribuable.

**Pour les développeurs d’applications (et les administrateurs informatiques) :**

Les administrateurs informatiques peuvent configurer les applications .NET 3,5 pour qu’elles s’exécutent sur .NET 3,5 ou .NET 4,5 (en fonction de ce qui est déjà installé). Pour exécuter une application gérée sur 3,5 ou 4,5, ajoutez simplement une section dans le fichier de configuration de l’application. Cela permet de s’assurer que si .NET 3,5 est installé, l’application s’exécutera sur .NET 3,5. dans le cas contraire, l’application s’exécutera sur .NET 4,5. Vous trouverez ci-dessous un exemple de la section supplémentaire dans le fichier de configuration :


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**Pour les OEM d’entreprise :**

pour activer .NET Framework 3,5 pour les builds EEAP et pour les applications qui n’ont pas accès à Windows Update :

1.  Copiez les \\ sources \\ côte \\ à côte de l’image ISO de build de système d’exploitation montée dans le dossier dotnet35 ou similaire. Par exemple :
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  Définissez la valeur de la RegKey :
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**Pour les entreprises :**

pour les ordinateurs configurés pour utiliser WSUS pour la maintenance, vous pouvez définir une entrée de registre pour permettre à l’ordinateur d’utiliser Windows Update pour l’activation de .net 3,5 au lieu de wsus (la maintenance sera toujours effectuée à partir de wsus si vous le faites).

-   Définissez la valeur de la RegKey :
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



Cette entrée de Registre peut également être définie via stratégie de groupe (stratégie de l’ordinateur local-> configuration de l’ordinateur-> système Modèles d’administration->. Sélectionnez le paramètre spécifier les paramètres pour l’installation des composants facultatifs et la réparation des composants.

si vous sélectionnez contacter Windows Update directement pour télécharger le contenu de réparation au lieu de Windows Server Update Services (WSUS), toute tentative d’ajouter des fonctionnalités de Windows (par exemple, .NET Framework 3,5) ou des fonctionnalités de réparation déclenchera des téléchargements de fichiers à partir de Windows Update. Les ordinateurs cibles requièrent un accès Internet et WU pour cette option. Les opérations de maintenance normales continuent à utiliser WSUS si elle a été configurée en tant que source.

**Note relative à la définition de l’emplacement source local via des entrées de Registre**

les administrateurs informatiques peuvent définir des emplacements sources locaux pour les fichiers .net 3,5 à l’aide d’une entrée de registre, afin que les utilisateurs puissent utiliser la boîte de dialogue ajouter/supprimer des composants Windows pour activer des fonctionnalités avec une charge utile manquante sans avoir à spécifier un emplacement source. La valeur de l’entrée de Registre peut être contrôlée via la stratégie de groupe.

Cette entrée de Registre est prise en charge :



<table>
<thead>
<tr class="header">
<th>Entrée</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Chemin de la source locale</td>
<td>REG_EXPAND_SZ</td>
<td>Chemin (s) source local à utiliser par défaut. Plusieurs chemins d’accès peuvent être spécifiés ; ils doivent être séparés par ;. Les emplacements sont recherchés dans l’ordre dans lequel ils sont spécifiés. <br/> Les emplacements sources locaux qui sont spécifiés sur la ligne de commande DISM ont la priorité sur les emplacements spécifiés dans cette entrée de registre. Les emplacements de dossier peuvent être spécifiés dans cette entrée de registre. <br/> Les fichiers WIM peut être utilisé, mais le chemin d’accès doit être au fichier WIM ; Il n’est pas nécessaire de le monter, par exemple : <br/> <dl> Wim : \\ machine\share\file.wim : 1<br />
</dl> Notez le 1 à la fin. Vous devez spécifier l’index numérique de l’image que vous souhaitez utiliser dans le fichier WIM. <br/> Pour un fichier WIM monté, le chemin source doit faire référence au répertoire Windows de l’image montée, plutôt qu’au point de montage (par exemple:/source : &lt; mount_point &gt; \Windows au lieu de/source &lt; : &gt; mount_point). <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>Ressources

<dl>

[Implémentation d’une stratégie basée sur le registre](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>
