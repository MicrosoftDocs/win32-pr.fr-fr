---
description: Utilisation de SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Utilisation de SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a627e50c6be3a3e8636378890025a6dde091948954e2709935c7dc84fa30c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655029"
---
# <a name="using-symsrv"></a>Utilisation de SymSrv

SymSrv fournit des fichiers de symboles à partir de magasins de symboles centralisés. Ces magasins peuvent contenir un nombre quelconque de fichiers de symboles, correspondant à un nombre quelconque de programmes ou de systèmes d’exploitation. Les magasins peuvent également contenir des fichiers binaires, qui sont particulièrement utiles lors du débogage de fichiers minidump.

Les magasins peuvent contenir les véritables fichiers de symboles et binaires, ou simplement pointeurs vers des fichiers de symboles. Si le magasin contient des pointeurs, SymSrv récupère les fichiers réels directement à partir de leurs sources.

SymSrv peut également séparer un magasin de symboles volumineux en un plus petit sous-ensemble adapté à une tâche de débogage spécialisée.

Enfin, SymSrv peut obtenir des fichiers de symboles à partir d’une source HTTP ou HTTPs à l’aide des informations de connexion fournies par le système d’exploitation. SymSrv prend en charge les sites HTTPs protégés par des cartes à puce, des certificats, des connexions et des mots de passe standard.

## <a name="setting-the-symbol-path"></a>Définition du chemin d’accès aux symboles

Comme décrit dans [chemins](symbol-paths.md)d’accès aux symboles, le chemin d’accès aux symboles ( \_ variable d’environnement du \_ \_ chemin d’accès aux symboles NT) peut être constitué de plusieurs éléments de chemin d’accès séparés par des points-virgules. Si un ou plusieurs de ces éléments de chemin d’accès commencent par le texte « SRV \* », l’élément est un serveur de symboles et utilise symsrv pour localiser les fichiers de symboles.

> [!Note]  
> Si le texte « SRV \* » n’est pas spécifié mais que l’élément de chemin d’accès réel est un magasin de serveurs de symboles, le gestionnaire de symboles agit comme si « SRV \* » avait été spécifié. Le gestionnaire de symboles effectue cette détermination en recherchant l’existence d’un fichier appelé « pingme.txt » dans le répertoire racine du chemin d’accès spécifié.

 

Tout comme les chemins d’accès aux symboles sont composés d’éléments de chemin d’accès aux symboles séparés par des points-virgules, les serveurs de symboles sont composés d’éléments de magasin de symboles séparés par des astérisques. Il peut y avoir jusqu’à 10 magasins de symboles après le \* préfixe « SRV ». Les magasins répertoriés à gauche de la liste sont appelés magasins en *aval* et magasins à droite sont appelés magasins en *amont* .

<dl> \**SymbolStore* SRV  
SRV \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Si un seul élément du magasin de symboles est inclus dans le chemin d’accès, SymSrv essaie d’utiliser le fichier demandé directement à partir de ce magasin.

S’il y a deux magasins de symboles dans le chemin, SymSrv recherche le fichier de symboles dans le magasin de symboles le plus à gauche. Si le fichier est présent, il est utilisé. Si ce n’est pas le cas, SymSrv regarde immédiatement dans le magasin de symboles. Si le fichier est présent, il est copié dans le magasin gauche et ouvert à partir de cet emplacement.

S’il y a plus de deux magasins, ce comportement continue vers la droite jusqu’à ce que le fichier soit trouvé ou qu’il n’y ait plus de magasins dans la liste.

Le fichier n’est jamais ouvert à partir d’un magasin, mais du magasin le plus à gauche. Si le fichier est trouvé n’importe où dans la chaîne, il est copié dans chaque magasin à gauche de celui-ci. Ce processus de copie est appelé « en cascade » et offre certains avantages qui seront clarfied plus loin dans ce document.

## <a name="types-of-symbol-stores"></a>Types de magasins de symboles

Le tableau suivant présente des exemples des types de magasins de symboles pris en charge.

|  Type de magasin de symboles       |  Description |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\partage de serveur \\          | Chemin UNC complet d’un partage sur un serveur distant.                                                                                                                                                                                                                                                                                                 |
| c : \\ localCache             | Chemin d’accès à un répertoire sur l’ordinateur client.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | URL d’un site Web hébergeant les symboles. Doit être le magasin le plus à droite dans la liste et ne doit pas être le seul magasin de la liste.                                                                                                                                                                                                                          |
| https://SecureInternetSite | URL d’un site Web sécurisé hébergeant les symboles. cela peut prendre en charge les mots de passe, les Windows les informations d’identification de connexion, les certificats et les cartes à puce. Doit être le magasin le plus à droite dans la liste et ne doit pas être le seul magasin de la liste.                                                                                                                              |
| <blank>              | S’il n’y a pas de texte entre deux astérisques, cela indique le *magasin en aval par défaut*. L’emplacement est défini en appelant [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). La valeur par défaut est un répertoire nommé « sym » situé juste en dessous du répertoire du programme de l’application appelante. C’est ce que l’on appelle parfois le *cache local par défaut*. |



 

Étant donné qu’il est impossible d’écrire dans un magasin de symboles HTTP, il doit s’agir du magasin le plus à droite dans la liste. Si un magasin de symboles HTTP se trouvait au milieu ou à gauche de la liste de magasins, il n’est pas possible de copier les fichiers qu’il contient et la chaîne sera rompue. En outre, étant donné que le gestionnaire de symboles ne peut pas ouvrir un fichier à partir d’un site Web, un magasin HTTP ne doit pas être le magasin le plus à gauche ou le seul magasin de la liste. Si SymSrv est toujours présenté avec ce chemin d’accès aux symboles, il tentera de le récupérer en copiant le fichier dans le magasin en aval par défaut et en l’ouvrant à partir de là, que le magasin en aval par défaut soit indiqué ou non dans le chemin d’accès aux symboles.

## <a name="examples"></a>Exemples

Pour utiliser SymSrv avec un magasin de symboles sur \\ \\ mybuilds \\ mysymbols, définissez le chemin d’accès aux symboles suivant :

**Set \_ NT \_ symbol \_ path = SRV \* \\ \\ mybuilds \\ mysymbols**

Pour définir le chemin d’accès aux symboles afin que le débogueur copie les fichiers de symboles d’un magasin de symboles sur \\ \\ mybuilds \\ mysymbols dans votre répertoire local c : \\ localsymbols, utilisez :

**Set \_ NT \_ symbol \_ path = SRV \* c : \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Pour définir le chemin d’accès aux symboles afin que le débogueur copie les fichiers de symboles d’un magasin de symboles sur \\ \\ mybuilds \\ mysymbols vers le magasin en aval par défaut (généralement c : \\ débogueurs \\ sym), utilisez :

**Set \_ NT \_ symbol \_ path = SRV \* \* \\ \\ mybuilds \\ mysymbols**

Pour utiliser un magasin en cascade, définissez le chemin d’accès aux symboles suivant :

**Set \_ NT \_ symbol \_ path = SRV \* c : \\ localsymbols \* \\ \\ NearbyServer \\ Store\*https://DistantServer**

Dans cet exemple, SymSrv recherche d’abord le fichier dans c : \\ localsymbols. S’il y figure, il retourne un chemin d’accès au fichier. Sinon, SymSrv recherche le fichier dans \\ \\ NearbyServer \\ Store. S’il y figure, SymSrv copie le fichier dans c : \\ localsymbols et retourne un chemin d’accès au fichier. s’il est introuvable, symsrv recherche le fichier dans https://DistantServer et, s’il y figure, symsrv le copie dans \\ \\ NearbyServer \\ Store, puis sur c : \\ localsymbols.

Ce dernier exemple montre comment la conception judicieuse d’un chemin d’accès aux symboles peut être utilisée pour optimiser le téléchargement de symboles. Si vous avez un site professionnel avec un groupe de débogueurs et qu’ils ont tous besoin d’obtenir des symboles à partir d’un emplacement distant, vous pouvez configurer un serveur commun avec un magasin de symboles près de tous les débogueurs. Puis, configurez chaque débogueur avec le chemin d’accès aux symboles ci-dessus. Le premier débogueur qui requiert une certaine version de foo. pdb le télécharge à partir de https://DistantServer vers \\ \\ NearbyServer \\ Store, puis vers son propre ordinateur dans c : \\ localsymbols. Le débogueur suivant qui requiert le même fichier peut le télécharger à partir de \\ \\ NearbyServer \\ Store, car il a déjà été téléchargé à cet emplacement par le débogueur précédent. Cette mise en cache à plusieurs niveaux économise beaucoup de temps et de bande passante réseau.

## <a name="microsoft-symbol-store"></a>Magasin de symboles Microsoft

Microsoft fournit un accès à un serveur de symboles Internet qui contient des fichiers de symboles pour les nombreuses versions du système d’exploitation Windows. Il n’est pas garanti que ce catalogue de symboles soit complet, mais il est complet. D’autres produits Microsoft sont également représentés.

le serveur de symboles Internet est rempli avec divers symboles de Windows pour les systèmes d’exploitation Microsoft Windows, y compris les correctifs logiciels, les Service packs, les Packages de correctifs cumulatifs de sécurité et les versions commerciales. des symboles sont également disponibles sur le serveur pour les versions bêta et Release candidates actuelles pour les produits Windows, ainsi que divers autres produits microsoft, tels que microsoft Internet Explorer.

Si vous avez accès à Internet pendant le débogage, vous pouvez configurer le débogueur pour télécharger des symboles selon les besoins au cours d’une session de débogage, plutôt que de télécharger des fichiers de symboles séparément avant une session de débogage. Les symboles sont téléchargés vers un emplacement de répertoire que vous spécifiez, puis le débogueur les charge à partir de là.

L’URL du magasin de symboles Microsoft est https://msdl.microsoft.com/download/symbols . L’exemple suivant montre comment définir le chemin d’accès aux symboles du débogueur (remplacez le chemin d’accès de votre magasin en aval par *c : \\ DownstreamStore*) :

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>Fichiers compressés

SymSrv est compatible avec les magasins de symboles qui contiennent des fichiers compressés, à condition que cette compression ait été préformée avec l’outil compress.exe qui a été distribué avec le Kit de ressources Windows Server 2003. Les fichiers compressés doivent avoir un trait de soulignement comme dernier caractère dans leurs extensions de fichier (par exemple, Module1. PD \_ ou Module2. db \_ ). Pour plus d’informations, consultez [utilisation de SymStore](using-symstore.md).

Lors de la cascade, les fichiers ne sont pas décompressés, sauf si le magasin cible est le magasin le plus à gauche dans le chemin d’accès. S’il n’existe qu’un seul magasin dans le chemin d’accès et qu’il contient un fichier compressé, SymSrv copie le fichier dans le magasin en aval par défaut et l’ouvre à partir de là, même si le magasin en aval par défaut n’est pas indiqué dans le chemin d’accès des symboles.

**DbgHelp 6,1 et versions antérieures. :** Si les fichiers du magasin principal sont compressés, vous devez utiliser un magasin en aval. SymSrv décompressera tous les fichiers avant de les copier dans le magasin en aval.

## <a name="deleting-the-cache"></a>Suppression du cache

Si vous utilisez un magasin en aval en tant que cache, vous pouvez supprimer ce répertoire à tout moment pour économiser de l’espace disque.

il est possible d’avoir un grand magasin de symboles qui comprend des fichiers de symboles pour de nombreux programmes ou versions de Windows. si vous mettez à niveau la version de Windows utilisée sur votre ordinateur cible, les fichiers de symboles mis en cache seront tous identiques à la version antérieure. Ces fichiers mis en cache ne seront plus utilisés et, par conséquent, cela peut être un bon moment pour supprimer le cache.

les outils de débogage pour Windows sont fournis avec un utilitaire appelé agestore.exe qui supprime de manière sélective les fichiers d’une arborescence de répertoires, en laissant les fichiers utilisés le plus récemment. Cet outil est conçu pour nettoyer les fichiers inutilisés des magasins de serveurs de symboles. Elle vous permet de contrôler de nombreuses options, notamment les algorithmes de date et d’ingestion de la taille de répertoire.

## <a name="flat-cache-directory"></a>Répertoire de cache plat

Il est possible de déclarer le magasin en aval par défaut comme un répertoire plat, plutôt qu’une structure d’arborescence de symboles standard. Pour ce faire, appelez la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) avec **le \_ \_ répertoire plat SYMOPT** (cela définit également l’option de **\_ magasin SSRVOPT plat \_ par défaut \_** dans symsrv). Veillez à appeler [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) avant d’effectuer cette procédure. dans le cas contraire, les fichiers de symboles peuvent être écrits dans le répertoire du programme.

## <a name="pointer-files"></a>Fichiers de pointeur

SymStore peut créer et utiliser des fichiers qui pointent vers un fichier cible plutôt que vers le fichier cible lui-même. Si un magasin de symboles contient un tel fichier pointeur, la valeur par défaut consiste à copier le fichier à partir de l’emplacement indiqué dans le fichier pointeur dans le magasin. Pour configurer un magasin de manière à ce que le fichier de pointeur soit copié à la place du fichier sur lequel il pointe, créez un fichier nommé wantsptr.txt à la racine du magasin cible. Le contenu de wantsptr.txt n’est pas important, seulement la présence du fichier.

## <a name="excluding-files-from-symbols-list"></a>Exclusion de fichiers d’une liste de symboles

Pour exclure des fichiers d’une recherche de symboles, vous pouvez spécifier leurs noms dans symsrv.ini ou dans le registre. Pour spécifier les fichiers dans symsrv.ini, créez une section nommée exclusions et répertoriez les fichiers. Les noms de fichiers peuvent contenir des caractères génériques, comme illustré dans l’exemple suivant :

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini doit se trouver dans le même répertoire que celui dans lequel symsrv.dll réside. Dans la plupart des installations, le fichier n’existe pas et vous devez en créer un nouveau.

Vous pouvez également stocker les fichiers à exclure dans le registre. Créez la clé de Registre suivante : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Symbol Server \\ exclusions**. Stockez chaque nom de fichier sous la forme d’une valeur de chaîne (REG \_ SZ) au sein de cette clé. Le nom de la valeur de chaîne spécifie le nom du fichier à exclure. Vous pouvez utiliser le contenu de la valeur de chaîne pour stocker un commentaire décrivant la raison pour laquelle le fichier est exclu.

## <a name="installation"></a>Installation

le serveur de symboles SymSrv (symsrv.dll) est inclus dans le package outils de débogage pour Windows. Il doit être installé dans le même répertoire que la copie de dbghelp.dll que vous chargez. Pour plus d’informations, consultez [appel de la bibliothèque dbghelp](calling-the-dbghelp-library.md).

 

 



