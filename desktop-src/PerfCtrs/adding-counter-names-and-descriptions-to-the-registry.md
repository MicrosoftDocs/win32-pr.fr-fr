---
description: Les noms et les descriptions de tous les objets de performance et de leurs compteurs sont stockés dans le registre.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Ajout de noms de compteurs et de descriptions au Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119106"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Ajout de noms de compteurs et de descriptions au Registre

> [!IMPORTANT]
> En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants pour utiliser cette méthode.

Les noms et les descriptions de tous les objets de performance v1 et de leurs compteurs doivent être installés sur le système. Pour stocker les noms et les descriptions des objets et des compteurs de votre [fournisseur v1](providing-counter-data.md):

- [Créez un fichier d’en-tête. h](#creating-a-symbolic-constants-h-file) contenant les constantes symboliques pour les décalages de vos objets et compteurs.
- [Créez un fichier d’initialisation (.INI)](#creating-an-initialization-ini-file) qui contient les chaînes.
- Lors de l’installation de votre composant, [Exécutez l’outil **lodctr**](#running-the-lodctr-tool) pour installer les noms et les descriptions dans le registre.
- Lors de la désinstallation de votre composant, exécutez l’outil unlodctr pour supprimer les noms et les descriptions du Registre.

## <a name="creating-a-symbolic-constants-h-file"></a>Création d’un fichier de constantes symboliques (. h)

Créez un fichier d’en-tête. h qui définit les constantes (macros) des décalages aux objets et aux compteurs fournis par votre fournisseur. L’en-tête. h est utilisé comme entrée pour **lodctr** pendant l’installation de votre fournisseur et peut également être utilisé par le code C/C++ de votre fournisseur.

Les valeurs de constante doivent être consécutives, même les nombres commençant par zéro. Regroupez les constantes par objets (par exemple, démarrez chaque groupe avec le décalage de l’objet, puis suivez les décalages des compteurs pour cet objet).

Les constantes dans l’en-tête déterminent l’ordre dans lequel les compteurs sont ajoutés au nom et au texte d’aide dans le registre. Le fournisseur utilise les offsets pour déterminer l’objet interrogé et les valeurs d’index à utiliser lors du retour des données. Pour plus d’informations, consultez [implémentation de OpenPerformanceData](implementing-openperformancedata.md).

L’exemple suivant illustre un fichier de constante symbolique, nommé CounterOffsets. h, qui est utilisé dans l’exemple [création d’une DLL d’extension de performances](creating-a-performance-extension-dll.md) .

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Création d’un fichier d’initialisation (.INI)

Le fichier d’initialisation (.INI) contient le nom et les chaînes d’aide pour chaque objet et compteur définis dans votre fichier de symboles. Le fichier .INI est utilisé comme entrée pour **lodctr** lors de l’installation de votre fournisseur.

Le fichier .INI doit être encodé au format UTF-16LE (avec la marque d’ordre d’octet) et doit avoir les sections et les clés suivantes :

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>section [info]

La `[info]` section contient des informations générales sur le fournisseur. Les clés de section sont définies comme suit :

|Clé|Description
|---|-----------
|**DriverName**| Spécifiez le nom de la clé de performance du fournisseur située dans le Registre sous la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` clé. Pour plus d’informations sur la création de cette clé, consultez [création de la clé de performance de l’application](creating-the-applications-performance-key.md).
|**SymbolFile**| Spécifiez le fichier d’en-tête. h qui contient les valeurs symboliques des objets et des compteurs de votre fournisseur. Pendant l’installation (lors de l’appel de **lodctr**), le fichier d’en-tête doit se trouver dans le même répertoire que le fichier .INI.
|**TPM**| Si vous incluez cette clé dans la `[info]` section, **lodctr** ajoute une valeur de registre de code de validation de bibliothèque à votre clé de performance avec une signature binaire de votre dll de performance. Lorsque PERFLIB appelle votre DLL, il compare la signature avec votre DLL pour déterminer si la DLL a été modifiée. La valeur de la clé **approuvée** est ignorée.

Les `DriverName` `SymbolFile` clés et sont requises.

### <a name="objects-section"></a>section [objets]

La `[objects]` section fournit une liste des objets de performance que le fournisseur prend en charge. Utilisé pour déterminer si chaque symbole de la `[text]` section fait référence à un objet ou à un compteur.

Pour chaque objet (CounterSet) pris en charge par votre fournisseur, ajoutez une clé nommée `<symbol>_<langid>_NAME=` à la `[objects]` section, où `<symbol>` est le nom de l’objet et `<langid>` est l’ID de langue de l’une des langues prises en charge. La valeur est ignorée.

> [!IMPORTANT]
> La `[objects]` section améliore les performances du système. Bien que la section objets soit facultative, vous devez toujours inclure cette section dans votre fichier de .INI. Si vous incluez cette section, votre DLL de performance est appelée uniquement si vous prenez en charge l’objet demandé. Si vous n’incluez pas la section objets, votre DLL est appelée pour chaque requête, car le système ne connaît pas les objets pris en charge par votre fournisseur. Si la section de l’objet n’est pas incluse, **lodctr** génère un message dans le journal des événements de l’application indiquant que le fichier .INI ne contenait pas de section objets. L’identificateur d’événement de ce message est 2000.

### <a name="languages-section"></a>section [languages]

La `[languages]` section fournit une liste des identificateurs de langue de chaque langue pour laquelle votre fournisseur fournit des chaînes de nom et d’aide. Tous les fournisseurs doivent prendre en charge `009` (anglais).

Pour chaque langue prise en charge, ajoutez une clé nommée `<langid>=` . La valeur est ignorée, mais à des fins de documentation, la valeur est normalement définie sur le nom de la langue correspondante, par exemple `009=English` .

Pour la plupart des langues, vous devez utiliser l’identificateur de langue principal. La liste complète des identificateurs de langue se trouve dans le fichier d’en-tête Winnt. h, sous le titre « ID de langue principale ». Convertit la valeur trouvée dans Winnt. h en une séquence de 3 chiffres hexadécimaux en supprimant le `0x` préfixe et en ajoutant des chiffres de début `0` jusqu’à ce que la séquence ait une longueur de 3 chiffres. Par exemple, pour spécifier des chaînes en anglais (0x9), utilisez 009. Pour spécifier des chaînes italiennes (0x10), utilisez 010.

Les langages chinois et portugais nécessitent à la fois les identificateurs principal et de sous-langue. Utilisez 404, 804, 416 ou 816 au lieu de 004 ou 016.

### <a name="text-section"></a>section [Text]

La `[text]` section fournit le nom et les chaînes d’aide pour vos objets et compteurs.

Pour chaque objet ou compteur, et pour chaque langue prise en charge, vous devez fournir une clé de nom (contenant le nom ou la chaîne de titre pour votre objet ou compteur) et vous pouvez éventuellement fournir une clé d’aide (contenant la description ou la chaîne d’explication pour votre objet ou compteur). Les clés doivent être nommées `<symbol>_<langid>_NAME` et `<symbol>_<langid>_HELP` , où `<symbol>` est la constante symbolique pour l’objet ou le compteur (tel que défini dans le fichier. h de constante symbolique) et `<langid>` est l’identificateur de langue utilisé pour cette chaîne.

Par exemple, les chaînes en anglais pour un compteur avec Symbol `MY_COUNTER` sont spécifiées comme suit :

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Les touches de texte peuvent apparaître dans n’importe quel ordre. Les chaînes de texte ne doivent pas contenir de caractères de mise en forme tels que des tabulations.

### <a name="example-ini-file"></a>Exemple de fichier INI

Voici un exemple de fichier d’initialisation utilisé dans l’exemple de [création d’une DLL d’extension de performances](creating-a-performance-extension-dll.md) .

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Exécution de l’outil lodctr

Pour charger les noms et les chaînes d’aide définis dans votre fichier .INI (au cours de l’installation de votre fournisseur), exécutez l’outil **lodctr** à partir du dossier qui contient votre fichier .INI et votre fichier d’en-tête. L’outil est inclus avec l’ordinateur. Vous devez exécuter **lodctr** avec des privilèges élevés. Le paramètre de **lodctr** est le chemin d’accès à votre fichier .INI. Par exemple : `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Pour décharger les chaînes de noms et d’aide (pendant la désinstallation), exécutez l’outil **unlodctr** . Vous devez exécuter **unlodctr** avec des privilèges élevés. Le paramètre de **unlodctr** est le DriverName de votre fournisseur (nom de la clé de performance du fournisseur). Par exemple : `unlodctr "MyProvider"`.

Avant d’exécuter **lodctr**, assurez-vous que votre application comporte une entrée sous la clé **services** . Pour plus d’informations, consultez [création de la clé de performance de l’application](creating-the-applications-performance-key.md). Si la clé n’existe pas, **lodctr** ne met pas à jour le Registre avec vos noms et descriptions.

Comme alternative à l’exécution de **lodctr**, vous pouvez appeler [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (défini dans loadperf. h) à partir de votre programme d’installation pour charger les descriptions des noms de compteur. Vous pouvez ensuite appeler [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) pendant la désinstallation.

L’utilitaire **lodctr** copie les chaînes du fichier .INI vers les **compteurs** et les valeurs de registre de l' **aide** sous les sous-clés de langue appropriées. Si la sous-clé de langue correspondante n’existe pas, les chaînes de cette langue ne sont pas copiées. L’utilitaire met également à jour le **dernier compteur** et la **dernière valeur d’aide** . Les noms et les descriptions des compteurs de performances sont stockés à l’emplacement suivant dans le registre.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Outre l’ajout de valeurs sous la clé **Perflib** , l’outil **lodctr** ajoute également les valeurs suivantes au nœud **services** de l’application. Dans la plupart des cas, l’application et le fournisseur auront une relation un-à-un. Toutefois, un fournisseur peut fournir des données de compteur pour plusieurs applications, ce qui explique pourquoi la clé est basée sur l’application et non sur le fournisseur.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
