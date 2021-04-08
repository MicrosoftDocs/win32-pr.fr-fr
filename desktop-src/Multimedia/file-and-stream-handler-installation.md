---
title: Installation du gestionnaire de fichiers et de flux
description: Installation du gestionnaire de fichiers et de flux
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675265"
---
# <a name="file-and-stream-handler-installation"></a>Installation du gestionnaire de fichiers et de flux

La bibliothèque AVIFile utilise des gestionnaires de fichiers et de flux installés pour la lecture et l’écriture de fichiers AVI et de flux. Un gestionnaire est installé lorsqu’il se trouve dans le répertoire système de Windows et le registre contient les informations suivantes requises pour décrire et identifier un gestionnaire :

-   Identificateur de classe de 16 octets pour le gestionnaire
-   Brève description du gestionnaire
-   Nom du fichier contenant le gestionnaire
-   Extension de fichier qu’un gestionnaire de fichiers peut traiter
-   Accès aux fichiers et autres propriétés associés à un gestionnaire de fichiers
-   Codes à quatre caractères identifiant les types de flux qu’un gestionnaire de flux peut traiter

La bibliothèque AVIFile interroge le registre pour les gestionnaires qui sont externes à une application lors de l’ouverture de fichiers et de l’accès aux flux. Le résultat d’une requête réussie retourne le nom de fichier d’un gestionnaire qui peut traiter le fichier ou le type de flux spécifié dans la requête. Le Registre répertorie chaque gestionnaire en créant trois entrées de la forme suivante :


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



Ces entrées se composent des éléments suivants.



| Partie                                   | Description                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_racine des classes HKEY \_                    | Identifie l’entrée racine du Registre.                                                                                                                                               |
| Clsid                                  | Identifie cette entrée en tant qu’identificateur de classe.                                                                                                                                             |
| {00010023-0000-0000-C000-000000000046} | Spécifie un identificateur d’interface (IID) ou un identificateur de classe. Cette valeur est un identificateur unique de 16 octets. (L’identificateur peut également être appelé GUID ou UUID dans d’autres manuels.) |
| Lecteur/enregistreur de fichier Wave                | Spécifie une chaîne pour décrire le gestionnaire. Cette chaîne peut être affichée dans les boîtes de dialogue permettant de sélectionner des gestionnaires de fichiers et de flux.                                                         |
| InProcServer32                         | Spécifie le fichier (dans cet exemple, WAVEFILE.DLL) qui peut être chargé pour gérer cette classe.                                                                                              |
| AVIFile                                | Spécifie les propriétés d’un gestionnaire de fichiers. Dans cet exemple, le gestionnaire peut lire et écrire dans un fichier AVI.                                                                              |



 

Un gestionnaire de fichiers peut avoir une ou plusieurs de ses propriétés stockées dans le registre. Les constantes suivantes identifient les propriétés actuellement associées à un fichier.



| Constante                        | Description                                                          |
|---------------------------------|----------------------------------------------------------------------|
| AVIFILEHANDLER \_ CANACCEPTNONRGB | Indique qu’un gestionnaire de fichiers peut traiter des données d’image autres que RVB. |
| AVIFILEHANDLER \_ CANREAD         | Indique qu’un gestionnaire de fichiers peut ouvrir un fichier avec un accès en lecture.      |
| AVIFILEHANDLER \_ CANWRITE        | Indique qu’un gestionnaire de fichiers peut ouvrir un fichier avec un accès en écriture.     |



 

Lorsque vous créez un gestionnaire de fichiers ou de flux, vous pouvez obtenir un nouvel identificateur en exécutant UUIDGEN.EXE. Utilisez toujours UUIDGEN.EXE pour créer un nouvel identificateur. Le nombre hexadécimal de 16 octets créé par cet exécutable identifie de manière unique votre gestionnaire.

La bibliothèque AVIFile utilise des entrées supplémentaires dans le registre pour identifier un identificateur de classe en fonction de l’extension de fichier qu’un gestionnaire de fichiers peut traiter ou d’un code à quatre caractères qu’un gestionnaire de fichiers ou de flux peut traiter. Par exemple, les entrées suivantes associent un identificateur de classe à l’extension de fichier. WAV et le code à quatre caractères « WAVE » :


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Ces entrées se composent des éléments suivants.



| Partie                                   | Description                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| \_racine des classes HKEY \_                    | Identifie l’entrée racine du Registre.                                                        |
| AVIFile                                | Identifie cette entrée en tant qu’entrée utilisée par AVIFile.                                                |
| Extensions                             | Spécifie l’extension de fichier (dans cet exemple,. WAV) qu’un gestionnaire de fichiers peut traiter.             |
| RIFFHandlers                           | Spécifie le code à quatre caractères (dans cet exemple, « WAVE ») qu’un gestionnaire de fichiers ou de flux peut traiter. |
| {00010023-0000-0000-C000-000000000046} | Spécifie un identificateur d’interface (IID) ou un identificateur de classe.                                      |



 

Si vous distribuez votre flux ou votre gestionnaire de fichiers sans application d’installation pour l’installer dans le système de l’utilisateur, vous devez inclure un. Fichier REG pour que l’utilisateur puisse installer le gestionnaire. L’utilisateur utilisera l’éditeur du Registre pour créer des entrées de Registre pour votre flux ou votre gestionnaire de fichiers.

L’exemple suivant montre le contenu d’un type standard. Fichier REG. La première entrée de l’exemple suivant est la chaîne descriptive du gestionnaire. La deuxième entrée identifie le fichier contenant le gestionnaire. La troisième entrée identifie les propriétés du gestionnaire de fichiers (dans ce cas, l’accès en lecture seule aux fichiers). La quatrième entrée associe le type de fichier traité par le gestionnaire (dans ce cas, les fichiers avec un. Extension de nom de fichier JPG) avec l’identificateur de classe.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Lors de la création de ce fichier, enregistrez-le avec un. Extension REG pour l’identifier comme fichier de mise à jour du Registre. Remplacez également un IID unique pour le code de 16 octets utilisé dans l’exemple.

 

 




