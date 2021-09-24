---
description: Le fichier Mt.exe est un outil qui génère des fichiers et des catalogues signés. elle est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows. Mt.exe nécessite que le fichier référencé dans le manifeste soit présent dans le même répertoire que le manifeste.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8987b4b78a85248eb085b8acf45b1fd364a5da
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521021"
---
# <a name="mtexe"></a>Mt.exe

Le fichier Mt.exe est un outil qui génère des fichiers et des catalogues signés. elle est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows. Mt.exe nécessite que le fichier référencé dans le manifeste soit présent dans le même répertoire que le manifeste.

Mt.exe génère des hachages à l’aide de l’implémentation CryptoAPI de l’algorithme de hachage sécurisé (SHA-1). Pour plus d’informations sur les algorithmes de hachage, consultez [Algorithmes de hachage et de signature](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Les hachages sont insérés sous la forme d’une chaîne hexadécimale dans les balises de **fichier** du manifeste. L’outil génère actuellement uniquement des hachages SHA-1, bien que les fichiers dans les manifestes puissent utiliser d’autres schémas de hachage.

Mt.exe utilise Makecat.exe pour générer des fichiers catalogue (. cat) à partir de fichiers de définition de catalogue (. CDF). Cet outil remplit un fichier CDF de modèle standard avec le nom et l’emplacement de votre manifeste. Vous pouvez l’utiliser avec Makecat.exe pour générer le catalogue d’assembly.

la version de Mt.exe fournie dans les versions récentes du SDK Windows peut également être utilisée pour générer des manifestes pour les assemblys managés et les assemblys côte à côte non managés.

## <a name="syntax"></a>Syntaxe

```console
mt.exe [-manifest:<component1.manifest><component2.manifest>] [-identity:<identity string>] 
[-rgs:<file1.rgs>] [-tlb:<file2.tlb>] [-dll:<file3.dll>] [-replacements:<XML filename>]
[-managedassemblyname:<managed assembly>] [-nodependency] [-category] [-out:<output manifest name>]
[-inputresource:<file4>;[#]<resource_id>] [-outputresource:<file5>;[#]<resource_id>] 
[-updateresource:<file6>;[#]<resource_id>] [-hashupdate[:<path to files>]] [-makecdfs] [-validate_manifest]
[-validate_file_hashes:<path to files>] [-canonicalize] [-check_for_duplicates] [-nologo] [-verbose]
```

## <a name="command-line-options"></a>Options de la ligne de commande

Mt.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.



<table>
                    <tr>
                        <th>Option</th>
                        <th>Description</th>
                    </tr>
                    <tr>
                        <td>-manifest</td>
                        <td><p>Spécifie le nom du fichier manifeste. Pour modifier un manifeste unique, spécifiez un nom de fichier manifeste.  Par exemple, composant. manifest.</p> <p>Pour fusionner plusieurs manifestes, spécifiez les noms des manifestes sources ici.  Spécifiez le nom du manifeste mis à jour avec les options <i>-out</i>, <i>-outputresource</i>ou <i>-UpdateResource</i>  .  Par exemple, la ligne de commande suivante demande une opération qui fusionne deux manifestes, man1. manifest et man2. manifest, dans un nouveau manifeste, man3. manifest.</p><p><i>mt.exe-manifest man1. manifeste man2. manifester : man3. manifest</i></p><p>Aucun signe deux-points ( :) est requis avec l’option <i>-Manifest</i> .</p></td>
                    </tr>
                    <tr>
                        <td>-identité</td>
                        <td><p>Fournit les valeurs des attributs de l’élément <strong>assemblyIdentity</strong> du manifeste. L’argument de l’option <i>-Identity</i> est une valeur de chaîne qui contient les valeurs d’attribut dans les champs séparés par des virgules.  Indiquez la valeur de l’attribut <strong>Name</strong> dans le premier champ, sans inclure de sous-chaîne "Name =". Tous les champs restants spécifient les attributs et leurs valeurs à l’aide de la forme : &lt; nom d’attribut &gt; = &lt; ATTRIBUTE_VALUE &gt; .</p><p>Par exemple, pour mettre à jour l’élément <strong>assemblyIdentity</strong> du manifeste avec les informations suivantes :</p><p>&lt;assemblyIdentity type = "Win32" Name = "Microsoft. Windows. SampleAssembly "version =" 6.0.0.0 "processorArchitecture =" x86 "publicKeyToken =" a5aaf5ba15723d5 "/&gt; </p><p>incluez l’option <i>-Identity</i> suivante sur la ligne de commande :</p><p><i>-Identity :</i>«Microsoft. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, type = Win32, publicKeyToken = a5aaf5ba15723d5»</p></td>
                    </tr>
                    <tr>
                        <td>-RGS </td>
                        <td><p>Spécifie le nom du fichier de script d’inscription (. RGS). L’option <i>-dll  </i>est requise pour utiliser l’option <i>-RGS</i> .</p> </td>
                    </tr>
                    <tr>
                        <td>-TLB </td>
                        <td><p>Spécifie le nom du fichier de bibliothèque de types (.tlb).  L’option <i>-dll  </i>est requise pour utiliser l’option <i>-TLB</i> .</p> </td>
                    </tr>
                    <tr>
                        <td>-dll </td>
                        <td><p>Spécifie le nom du fichier de bibliothèque de liens dynamiques (DLL). L’option <i>-dll  </i>est requise par <i>mt.exe </i> si les options <i>-RGS</i> ou <i>-TLB</i> sont utilisées. Spécifiez le nom de la DLL que vous envisagez de générer à partir des fichiers. RGS ou. tlb.</p><p>Par exemple, la commande suivante demande une opération qui génère un manifeste à partir de fichiers. RGS et. tlb.</p><p><i>mt.exe-RGS : testreg1. RGS-TLB : testlib1. tlb-dll:test.dll-remplacements : Rep. manifest-Identity : "Microsoft. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, type = Win32, publicKeyToken = a5aaf5ba15723d5 "-out : rgstlb. manifest</i> </p> </td>
                    </tr>
                    <tr>
                        <td>-remplacements </td>
                        <td><p>Spécifie le fichier qui contient des valeurs pour la chaîne remplaçable dans le fichier. RGS.</p> </td>
                    </tr>
                    <tr>
                        <td>-managedassemblyname </td>
                        <td><p>Génère un manifeste à partir de l’assembly managé spécifié.  Utilisez avec l’option <i>-nodependency</i> pour générer un manifeste sans éléments de dépendance. Utilisez avec l’option <i>-Category</i> pour générer un manifeste avec des balises de catégorie. Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le fichier out. manifest à partir de managed.dll.</p><p><i>mt.exe-managedassemblyname:managed.dll : out. manifest </i></p> </td>
                    </tr>
                    <tr>
                        <td>-nodépendance </td>
                        <td><p>Spécifie une opération qui génère un manifeste sans éléments de dépendance.  L’option <i>-nodependency</i> requiert l’option <i>-managedassemblyname</i> . Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le manifeste out. à partir de managed.dll sans informations de dépendance.</p><p><i>mt.exe-managedassemblyname:managed.dll : out. manifest-nodependency</i></p> </td>
                    </tr>
                    <tr>
                        <td>-catégorie </td>
                        <td><p>Spécifie une opération qui génère un manifeste avec des balises de catégorie. L’option <i>-Category</i> requiert l’option <i>-managedassemblyname</i> . Par exemple, si managed.dll est un assembly managé, la ligne de commande suivante génère le fichier out. manifest à partir de managed.dll avec des balises de catégorie.</p><p><i>mt.exe-managedassemblyname:managed.dll : out. manifest-catégorie</i></p> </td>
                    </tr>
                    <tr>
                        <td>-nologo</td>
                        <td><p>Spécifie une opération exécutée sans afficher les données de copyright Microsoft standard. Si  <i>mt.exe</i> s’exécute dans le cadre d’un processus de génération, cette option peut être utilisée pour empêcher l’écriture d’informations indésirables dans les fichiers journaux. </p></td>
                    </tr>
                    <tr>
                        <td>-out </td>
                        <td><p>Spécifie le nom du manifeste mis à jour.  S’il s’agit d’une opération à manifeste unique et que l’option <i>-out</i> est omise, le manifeste d’origine est modifié. </p></td>
                    </tr>
                    <tr>
                        <td>-inputresource </td>
                        <td><p>Spécifie une opération effectuée sur un manifeste obtenu à partir d’une ressource de type RT_MANIFEST.  Si l’option <i>-inputresource</i> est utilisée sans spécifier l’identificateur de ressource, &lt; resource_id &gt; , l’opération utilise la valeur CREATEPROCESS_MANIFEST_RESOURCE. </p><p>Par exemple, la commande suivante demande une opération qui fusionne un manifeste à partir d’une DLL, d' dll_with_manifest.dll et d’un fichier manifeste, man2. manifest.  Les manifestes fusionnés sont reçus par un manifeste dans le fichier de ressources d’une autre DLL, dll_with_merged_manifests. </p><p><i>mt.exe-inputresource:dll_with_manifest.dll ; #1-manifest man2. manifest-outputresource:dll_with_merged_manifest.dll ; #3</i></p><p>Pour extraire le manifeste d’une DLL, spécifiez le nom du fichier DLL.  Par exemple, la commande suivante extrait le manifeste à partir de lib1.dll et man3. manifest reçoit le manifeste extrait.</p><p><i>mt.exe-inputresource:lib.dll ; #1 : man3. manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-outputresource </td>
                        <td><p>Spécifie une opération qui génère un manifeste à recevoir par une ressource de type RT_MANIFEST.  Si l’option <i>-outputresource</i> est utilisée sans spécifier l’identificateur de ressource, &lt; resource_id &gt; , l’opération utilise la valeur CREATEPROCESS_MANIFEST_RESOURCE. </p></td>
                    </tr>
                    <tr>
                        <td>-UpdateResource </td>
                        <td><p>Spécifie une opération équivalente à l’utilisation des options <i>-inputresource</i>  et <i>-outputresource</i> avec des arguments identiques. Par exemple, la commande suivante demande une opération qui calcule un hachage des fichiers dans le chemin d’accès spécifié et met à jour le manifeste d’une ressource d’un fichier exécutable portable (PE, Portable Executable).</p><p><i>mt.exe-updateresource:dll_with_manifest.dll ; #1-hashupdate : f : \Files</i>.</p> </td>
                    </tr>
                    <tr>
                        <td>-hashupdate </td>
                        <td><p>Calcule la valeur de hachage des fichiers aux chemins d’accès spécifiés et met à jour la valeur de l’attribut de <strong>hachage</strong> de l’élément <strong>file</strong> avec cette valeur. </p><p>Par exemple, la commande suivante demande une opération qui fusionne deux fichiers manifeste, man1. manifest et man2. manifest, et met à jour la valeur de l’attribut <strong>hash</strong> de l’élément <strong>file</strong> dans le manifeste qui reçoit les informations fusionnées, fusionnées. manifest.</p><p><i>mt.exe-manifest man1. manifeste man2. manifest-hashupdate : d : \filerepository-out : fusionné. manifest</i></p><p>Si les chemins d’accès aux fichiers ne sont pas spécifiés, l’opération recherche l’emplacement du manifeste spécifié pour recevoir la mise à jour. Par exemple, la commande suivante demande une opération qui calcule la valeur de hachage mise à jour à l’aide des fichiers trouvés en recherchant l’emplacement du fichier. manifest mis à jour.</p><p><i>mt.exe-manifest yourComponent. manifeste-hashupdate-out : updated. manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-validate_manifest </td>
                        <td><p>Spécifie une opération qui effectue une vérification de la syntaxe de la conformité du manifeste avec le schéma de manifeste.  Par exemple, la commande suivante demande une vérification pour valider la conformité de man1. manifest avec son schéma. </p><p><i>mt.exe manifeste man1. manifest-validate_manifest</i></p> </td>
                    </tr>
                    <tr>
                        <td>-validate_file_hashes </td>
                        <td><p>Spécifie une opération qui valide les valeurs de hachage des éléments de <strong>fichier</strong> du manifeste. Par exemple, la commande suivante demande une opération qui valide les valeurs de hachage de tous les éléments de  <strong>fichier</strong> de man1. manifest.</p><p><i>mt.exe-manifest man1. manifest-validate_file_hashes : "c ; \Files"</i></p> </td>
                    </tr>
                    <tr>
                        <td>-canonicaliser </td>
                        <td><p>Spécifie une opération pour mettre à jour le manifeste au format canonique. Par exemple, la commande suivante met à jour man1. manifest au format canonique.</p><p><i>mt.exe-manifeste man1. manifest</i></p> </td>
                    </tr>
                    <tr>
                        <td>-check_for_duplicates </td>
                        <td><p>Spécifie une opération qui vérifie si le manifeste contient des éléments en double. Par exemple, la commande suivante vérifie man1. manifest pour les éléments en double.</p><p><i>mt.exe-man1. manifest-check_for_duplicates</i></p> </td>
                    </tr>                   
                    <tr>
                        <td>-makecdfs</td>
                        <td><p>Génère des fichiers. CDF pour créer des catalogues.  Par exemple, la commande suivante demande une opération qui met à jour la valeur de hachage et génère un fichier. CDF.</p><p><i>mt.exe-manifest COMP1. manifeste-hashupdate-makecdfs-out : updated. manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-verbose</td>
                        <td>Affiche des informations détaillées sur le débogage. </td>
                    </tr>
                    <tr>
                        <td>-?</td>
                        <td>Quand elle est exécutée avec- ?, ou sans options et arguments, Mt.exe affiche le texte d’aide.</td>
                    </tr>
                </table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement d’assembly côte à côte](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

