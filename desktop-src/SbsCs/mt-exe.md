---
description: Le fichier Mt.exe est un outil qui génère des fichiers et des catalogues signés. elle est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows. Mt.exe nécessite que le fichier référencé dans le manifeste soit présent dans le même répertoire que le manifeste.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb81f3e0b7bf6b67236f1bd6037d1eceb11e0b89
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623905"
---
# <a name="mtexe"></a>Mt.exe

Le fichier Mt.exe est un outil qui génère des fichiers et des catalogues signés. elle est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows. Mt.exe nécessite que le fichier référencé dans le manifeste soit présent dans le même répertoire que le manifeste.

Mt.exe génère des hachages à l’aide de l’implémentation CryptoAPI de l’algorithme de hachage sécurisé (SHA-1). Pour plus d’informations sur les algorithmes de hachage, consultez [Algorithmes de hachage et de signature](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Les hachages sont insérés sous la forme d’une chaîne hexadécimale dans les balises de **fichier** du manifeste. L’outil génère actuellement uniquement des hachages SHA-1, bien que les fichiers dans les manifestes puissent utiliser d’autres schémas de hachage.

Mt.exe utilise Makecat.exe pour générer des fichiers catalogue (. cat) à partir de fichiers de définition de catalogue (. CDF). Cet outil remplit un fichier CDF de modèle standard avec le nom et l’emplacement de votre manifeste. Vous pouvez l’utiliser avec Makecat.exe pour générer le catalogue d’assembly.

la version de Mt.exe fournie dans les versions récentes du SDK Windows peut également être utilisée pour générer des manifestes pour les assemblys managés et les assemblys côte à côte non managés.

## <a name="syntax"></a>Syntax

**mt.exe \[ -Manifest** _<Composant1. manifeste><COMPONENT2. manifest>_ *_\] \[ -Identity :_* *<identity string> * **\] \[ -RGS :** _<fichier1. RGS>_* _\] \[ -TLB :_ *_<fichier2. tlb>_* _\] \[ -dll :_ *_<file3.dll_*>_\] \[ -remplacements :_ *_<XML filename>_* _\] \[ -managedassemblyname :_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -catégorie \] \[ -out :_ *_<output manifest name>_* _\] \[ -inputresource :_ *_<file4>_* _; \[ \# \]_ *_><0 ID de ressource \_><1_* _\] \[ -outputresource :_ *_<file5>_* _; \[ \# \]_ *_><2 ID de ressource \_><3_* _\] \[ -UpdateResource :_ *_<file6>_* _; \[ \# \]_ *_><4 ID de ressource \_><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -Validate \_ manifeste \] \[ -valider les \_ \_ hachages de_ *_<path to files>_* _\] \[ \] \[ \_ \_ \] \[ \] \[ fichier :-canonicaliser-Rechercher les doublons-nologo-verbose \]_*

## <a name="command-line-options"></a>Options de la ligne de commande

Mt.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>Spécifie le nom du fichier manifeste. Pour modifier un manifeste unique, spécifiez un nom de fichier manifeste. Par exemple, composant. manifest.<br/> Pour fusionner plusieurs manifestes, spécifiez les noms des manifestes sources ici. Spécifiez le nom du manifeste mis à jour avec les options <strong>-out</strong>, <strong>-outputresource</strong>ou <strong>-UpdateResource</strong> . Par exemple, la ligne de commande suivante demande une opération qui fusionne deux manifestes, man1. manifest et man2. manifest, dans un nouveau manifeste, man3. manifest.<br/> <strong>mt.exe-manifest man1. manifeste man2. manifester : man3. manifest</strong><br/>
<blockquote>
[!Note]<br />
Aucun signe deux-points ( :) est requis avec l’option <strong>-Manifest</strong> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identité</td>
<td>Fournit les valeurs des attributs de l’élément <strong>assemblyIdentity</strong> du manifeste. L’argument de l’option <strong>-Identity</strong> est une valeur de chaîne qui contient les valeurs d’attribut dans les champs séparés par des virgules. Indiquez la valeur de l’attribut <strong>Name</strong> dans le premier champ, sans inclure &quot; name = &quot; SUBSTRING. Tous les champs restants spécifient les attributs et leurs valeurs en utilisant le format : <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Par exemple, pour mettre à jour l’élément <strong>assemblyIdentity</strong> du manifeste avec les informations suivantes :<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> incluez l’option <strong>-Identity</strong> suivante sur la ligne de commande :<br/> <strong>-identité :</strong> &quot; Librairie. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, type = Win32, publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Spécifie le nom du fichier de script d’inscription (. RGS). L’option <strong>-dll</strong> est requise pour utiliser l’option <strong>-RGS</strong> .<br/></td>
</tr>
<tr class="even">
<td>-TLB</td>
<td>Spécifie le nom du fichier de bibliothèque de types (.tlb). L’option <strong>-dll</strong> est requise pour utiliser l’option <strong>-TLB</strong> .<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Spécifie le nom du fichier de bibliothèque de liens dynamiques (DLL). L’option <strong>-dll</strong> est requise par <strong>mt.exe</strong> si les options <strong>-RGS</strong> ou <strong>-TLB</strong> sont utilisées. Spécifiez le nom de la DLL que vous envisagez de générer à partir des fichiers. RGS ou. tlb.<br/> Par exemple, la commande suivante demande une opération qui génère un manifeste à partir de fichiers. RGS et. tlb.<br/> <strong>mt.exe-RGS : testreg1. RGS-TLB : testlib1. tlb -dll:test.dll-remplacements : Rep. manifest-Identity : &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, type = Win32, publicKeyToken = a5aaf5ba15723d5 &quot; : rgstlb. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-remplacements</td>
<td>Spécifie le fichier qui contient des valeurs pour la chaîne remplaçable dans le fichier. RGS.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Génère un manifeste à partir de l’assembly managé spécifié. Utilisez avec l’option <strong>-nodependency</strong> pour générer un manifeste sans éléments de dépendance. Utilisez avec l’option <strong>-Category</strong> pour générer un manifeste avec des balises de catégorie. Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le fichier out. manifest à partir de managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll : out. manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodépendance</td>
<td>Spécifie une opération qui génère un manifeste sans éléments de dépendance. L’option <strong>-nodependency</strong> requiert l’option <strong>-managedassemblyname</strong> . Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le manifeste out. à partir de managed.dll sans informations de dépendance.<br/> <strong>mt.exe -managedassemblyname:managed.dll : out. manifeste-nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-catégorie</td>
<td>Spécifie une opération qui génère un manifeste avec des balises de catégorie. L’option <strong>-Category</strong> requiert l’option <strong>-managedassemblyname</strong> . Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le fichier out. manifest à partir de managed.dll avec des balises de catégorie.<br/> <strong>mt.exe -managedassemblyname:managed.dll : out. manifest-catégorie</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Spécifie une opération exécutée sans afficher les données de copyright Microsoft standard. Si <strong>mt.exe</strong> s’exécute dans le cadre d’un processus de génération, cette option peut être utilisée pour empêcher l’écriture d’informations indésirables dans les fichiers journaux. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Spécifie le nom du manifeste mis à jour. S’il s’agit d’une opération à manifeste unique et que l’option <strong>-out</strong> est omise, le manifeste d’origine est modifié. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Spécifie une opération effectuée sur un manifeste obtenu à partir d’une ressource de type RT_MANIFEST. Si l’option <strong>-inputresource</strong> est utilisée sans spécifier l’identificateur de ressource, <em> <resource_id> </em> , l’opération utilise la valeur CREATEPROCESS_MANIFEST_RESOURCE. <br/> Par exemple, la commande suivante demande une opération qui fusionne un manifeste à partir d’une DLL, d' dll_with_manifest.dll et d’un fichier manifeste, man2. manifest. Les manifestes fusionnés sont reçus par un manifeste dans le fichier de ressources d’une autre DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll ; #1-manifest man2. manifest -outputresource:dll_with_merged_manifest.dll ; #3</strong><br/> Pour extraire le manifeste d’une DLL, spécifiez le nom du fichier DLL. Par exemple, la commande suivante extrait le manifeste à partir de lib1.dll et man3. manifest reçoit le manifeste extrait.<br/> <strong>mt.exe -inputresource:lib.dll ; #1 : man3. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Spécifie une opération qui génère un manifeste à recevoir par une ressource de type RT_MANIFEST. Si l’option <strong>-outputresource</strong> est utilisée sans spécifier l’identificateur de ressource, <em> <resource_id> </em> , l’opération utilise la valeur CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-UpdateResource</td>
<td>Spécifie une opération équivalente à l’utilisation des options <strong>-inputresource</strong> et <strong>-outputresource</strong> avec des arguments identiques. Par exemple, la commande suivante demande une opération qui calcule un hachage des fichiers dans le chemin d’accès spécifié et met à jour le manifeste d’une ressource d’un fichier exécutable portable (PE, Portable Executable).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll ; #1-hashupdate : f : \Files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcule la valeur de hachage des fichiers aux chemins d’accès spécifiés et met à jour la valeur de l’attribut de <strong>hachage</strong> de l’élément <strong>file</strong> avec cette valeur. <br/> Par exemple, la commande suivante demande une opération qui fusionne deux fichiers manifeste, man1. manifest et man2. manifest, et met à jour la valeur de l’attribut <strong>hash</strong> de l’élément <strong>file</strong> dans le manifeste qui reçoit les informations fusionnées, fusionnées. manifest.<br/> <strong>mt.exe-manifest man1. manifeste man2. manifest-hashupdate : d : \filerepository-out : fusionné. manifest</strong><br/> Si les chemins d’accès aux fichiers ne sont pas spécifiés, l’opération recherche l’emplacement du manifeste spécifié pour recevoir la mise à jour. Par exemple, la commande suivante demande une opération qui calcule la valeur de hachage mise à jour à l’aide des fichiers trouvés en recherchant l’emplacement du fichier. manifest mis à jour.<br/> <strong>mt.exe-manifest yourComponent. manifeste-hashupdate-out : updated. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Spécifie une opération qui effectue une vérification de la syntaxe de la conformité du manifeste avec le schéma de manifeste. Par exemple, la commande suivante demande une vérification pour valider la conformité de man1. manifest avec son schéma. <br/> <strong>mt.exe manifeste man1. manifest-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Spécifie une opération qui valide les valeurs de hachage des éléments de <strong>fichier</strong> du manifeste. Par exemple, la commande suivante demande une opération qui valide les valeurs de hachage de tous les éléments de <strong>fichier</strong> de man1. manifest.<br/> <strong>mt.exe-manifest man1. manifest-validate_file_hashes : &quot; c ; \Files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonicaliser</td>
<td>Spécifie une opération pour mettre à jour le manifeste au format canonique. Par exemple, la commande suivante met à jour man1. manifest au format canonique.<br/> <strong>mt.exe-manifeste man1. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Spécifie une opération qui vérifie si le manifeste contient des éléments en double. Par exemple, la commande suivante vérifie man1. manifest pour les éléments en double.<br/> <strong>mt.exe-man1. manifest-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Génère des fichiers. CDF pour créer des catalogues. Par exemple, la commande suivante demande une opération qui met à jour la valeur de hachage et génère un fichier. CDF.<br/> <strong>mt.exe-manifest COMP1. manifeste-hashupdate-makecdfs-out : updated. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Affiche des informations détaillées sur le débogage.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Quand elle est exécutée avec- ?, ou sans options et arguments, Mt.exe affiche le texte d’aide.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement d’assembly côte à côte](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

