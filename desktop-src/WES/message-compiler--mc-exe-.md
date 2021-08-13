---
title: Message Compiler (MC.exe)
description: Utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- EventLog (MC.exe) du message
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470939"
---
# <a name="message-compiler-mcexe"></a>Message Compiler (MC.exe)

Utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message. Le compilateur génère les fichiers de ressources de message auxquels votre application est liée.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Arguments communs aux fichiers de texte de message et aux fichiers manifeste](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Arguments spécifiques aux fichiers manifestes](#arguments-specific-to-manifest-files)
-   [Arguments spécifiques à la génération de code que votre fournisseur utiliserait pour consigner des événements](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Arguments spécifiques aux fichiers texte du message](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Arguments communs aux fichiers de texte de message et aux fichiers manifeste

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Affiche les informations d’utilisation du compilateur de message.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Utilisez cet argument pour que le compilateur définisse le bit client (bit 28) dans tous les ID de message. Pour plus d’informations sur le bit du client, consultez winerror. h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-** *encodage* CP
</dt> <dd>

Utilisez cet argument pour spécifier l’encodage de caractères utilisé pour tous les fichiers texte générés. Les noms valides sont « ANSI » (par défaut), « UTF-8 » et « UTF-16 ». Les encodages Unicode ajoutent une marque d’ordre d’octet.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extension* **-e**
</dt> <dd>

Utilisez cet argument pour spécifier l’extension à utiliser pour le fichier d’en-tête. Vous pouvez spécifier jusqu’à trois caractères d’extension, à l’exclusion du point. La valeur par défaut est. h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *chemin*
</dt> <dd>

Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le fichier d’en-tête généré. L'emplacement par défaut est le répertoire actif.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *longueur*
</dt> <dd>

Utilisez cet argument pour que le compilateur génère un avertissement si le message dépasse la *longueur* des caractères.

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *chemin d’accès*
</dt> <dd>

Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le script généré du compilateur de ressources (fichier. RC) et les fichiers. bin générés (ressources binaires) inclus dans le script du compilateur de ressources. L'emplacement par défaut est le répertoire actif.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-** *nom* z
</dt> <dd>

Utilisez cet argument pour remplacer le nom de base par défaut que le compilateur utilise pour les fichiers qu’il génère. La valeur par défaut consiste à utiliser le nom de base du fichier d’entrée de *nom* de fichier.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Fichier de manifeste d’instrumentation ou fichier texte de message. Le fichier doit exister dans le répertoire actif. Vous pouvez spécifier un fichier manifeste, un fichier texte de message ou les deux. Le nom de fichier doit inclure l’extension. La Convention consiste à utiliser une extension. Man pour les fichiers manifeste et une extension. MC pour les fichiers texte du message.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Arguments spécifiques aux fichiers manifestes

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s** *chemin d’accès*
</dt> <dd>

Utilisez cet argument pour créer une ligne de base de votre instrumentation. Spécifiez le chemin d’accès au dossier qui contient vos fichiers manifeste de base de référence. Pour les versions ultérieures, vous utiliseriez ensuite l’argument **-t** pour vérifier le nouveau manifeste par rapport à la ligne de base pour les problèmes de compatibilité.

**Avant la version 1.12.7051 de MC :** Non disponible

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *chemin d’accès*
</dt> <dd>

Utilisez cet argument lorsque vous créez une nouvelle version de votre manifeste et que vous souhaitez vérifier la compatibilité des applications par rapport à la ligne de base que vous avez créée à l’aide de l’argument **-s** . Le chemin d’accès doit pointer vers le dossier qui contient le. Fichiers BIN créés par l’opération de base (voir le commutateur **-s** ).

**Avant la version 1.12.7051 de MC :** Non disponible

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *chemin*
</dt> <dd>

Le compilateur ignore cet argument et valide automatiquement le manifeste.

**Avant la version 1.12.7051 de MC :** Utilisez cet argument pour spécifier le dossier qui contient le fichier de schéma Eventic. xsd, que le compilateur utilise pour valider votre manifeste. le SDK Windows inclut le fichier de schéma eventic. xsd dans le \\ dossier include. Si vous ne spécifiez pas cet argument, le compilateur ne valide pas votre manifeste.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *chemin*
</dt> <dd>

Le compilateur ignore cet argument.

**Avant la version 1.12.7051 de MC :** Utilisez cet argument pour spécifier le dossier qui contient le fichier Winmeta.xml. Le fichier Winmeta.xml contient les types d’entrée et de sortie reconnus, ainsi que les canaux, niveaux et OpCodes prédéfinis. le SDK Windows inclut le fichier Winmeta.xml dans le \\ dossier include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Arguments spécifiques à la génération de code que votre fournisseur utiliserait pour consigner des événements

Vous pouvez utiliser les arguments de compilateur suivants pour générer du code en mode noyau ou en mode utilisateur que vous pouvez utiliser pour consigner des événements. vous pouvez également demander que le compilateur génère du code pour prendre en charge l’écriture d’événements sur les ordinateurs antérieurs à Windows Vista. Si votre application est écrite en C#, le compilateur peut générer une classe C# que vous pouvez utiliser pour consigner les événements. ces arguments sont disponibles à partir de la version MC 1.12.7051 livrée avec la version Windows 7 du kit de développement logiciel (SDK) windows.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-Co**
</dt> <dd>

Utilisez cet argument pour que le service de journalisation appelle votre fonction définie par l’utilisateur pour chaque événement que vous journalisez (la fonction est appelée une fois que l’événement a été enregistré). Votre fonction définie par l’utilisateur doit avoir la signature suivante.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



Vous devez également inclure la directive suivante dans votre code.

`#define MCGEN_CALLOUT pFnUserFunction`

Vous devez conserver votre implémentation aussi rapidement que possible pour éviter les problèmes de journalisation ; le service ne consigne plus vos événements tant que la fonction n’est pas retournée.

Vous pouvez utiliser cet argument avec l’argument **-km** ou **-um** .

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs (espace de** *noms* )
</dt> <dd>

Utilisez cet argument pour que le compilateur génère une classe C# basée sur la classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-espace de** *noms* CSS
</dt> <dd>

Utilisez cet argument pour que le compilateur génère une classe C# statique basée sur la classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Utilisez cet argument pour que le compilateur génère le code en mode noyau que vous utiliseriez pour enregistrer les événements définis dans votre manifeste.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-MOF**
</dt> <dd>

Déconseillé. utilisez cet argument pour que le compilateur génère du code que vous pouvez utiliser pour consigner les événements sur les ordinateurs antérieurs à Windows Vista. Cette option crée également un fichier MOF qui contient les classes MOF pour chaque événement défini dans le manifeste. Pour inscrire les classes dans le fichier MOF afin que les consommateurs puissent décoder les événements, utilisez le compilateur MOF (Mofcomp.exe). Pour plus d’informations sur l’utilisation du compilateur MOF, consultez [format MOF](/windows/desktop/WmiSdk/managed-object-format--mof-).

Pour utiliser ce commutateur, vous devez respecter les restrictions suivantes :

-   Chaque définition d’événement doit inclure les attributs Task et opcode
-   Chaque tâche doit inclure l’attribut eventGuid
-   Les données de modèle que les références d’événement ne peuvent pas contenir :
    -   Éléments de données qui spécifient les types d’entrée Win : Binary ou Win : SYSTEMTIME
    -   Structures
    -   Tableaux de taille variable ; Toutefois, vous pouvez spécifier des tableaux de longueur fixe
    -   Les types de données String ne peuvent pas spécifier l’attribut length

Vous devez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km**

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *préfixe*
</dt> <dd>

Utilisez cet argument pour remplacer le préfixe par défaut que le compilateur utilise pour l’enregistrement des noms de macros et de méthodes. Le préfixe par défaut est « EventWrite ». La chaîne est sensible à la casse.

Vous pouvez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km** .

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *préfixe*
</dt> <dd>

Utilisez cet argument pour supprimer des caractères au début du nom symbolique que vous avez spécifié pour l’événement. La comparaison respecte la casse. Le compilateur utilise le nom symbolique pour former les noms de macros et de méthodes de journalisation.

Le nom par défaut d’une macro de journalisation est EventWrite *SymbolName*, où *SymbolName* est le nom symbolique que vous avez spécifié pour l’événement. Par exemple, si vous affectez à l’attribut symbol de l’événement la valeur PrinterConnection, le nom de la macro est EventWritePrinterConnection. Pour supprimer l’imprimante du nom, utilisez l' **imprimante** **-P** , qui se traduit par EventWriteConnection.

Vous pouvez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km** .

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Utilisez cet argument pour que le compilateur génère le code en mode utilisateur que vous utiliseriez pour enregistrer les événements définis dans votre manifeste.

</dd> </dl>

Pour que le compilateur génère du code de journalisation, vous devez spécifier l’argument **-um**, **-CS**, **-CSS** ou **-km** . ces arguments s’excluent mutuellement.

Pour spécifier où placer les fichiers. h,. cs et. mof générés par le compilateur, utilisez l’argument **-h** . Si vous ne spécifiez pas l’argument **-h** , les fichiers sont placés dans le dossier actif.

Pour spécifier où placer le fichier. RC et les fichiers binaires (qui contiennent les ressources de métadonnées) générés par le compilateur, utilisez l’argument **-r** . Si vous ne spécifiez pas l’argument **-r** , les fichiers sont placés dans le dossier actif.

Le compilateur utilise le nom de base du fichier d’entrée comme nom de base des fichiers qu’il génère. Pour spécifier un nom de base, utilisez l’argument **-z** .

### <a name="arguments-specific-to-message-text-files"></a>Arguments spécifiques aux fichiers texte du message

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

utilisez cet argument pour spécifier que le fichier d’entrée de *nom* de fichier contient le contenu dans la page de codes Windows par défaut du système (CP_ACP). Il s’agit de la valeur par défaut. Utilisez **-u** pour Unicode. Si le fichier d’entrée contient une nomenclature, cet argument est ignoré.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Déconseillé. Utilisez cet argument pour spécifier que les messages dans le fichier output. bin doivent être au format ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Utilisez cet argument pour que le compilateur utilise le nom de base du fichier d’entrée de *nom* de fichier pour les noms de fichiers. bin. La valeur par défaut consiste à utiliser « MSG ».

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Utilisez cet argument pour utiliser des valeurs décimales pour les constantes de gravité et de fonction dans le fichier d’en-tête au lieu de valeurs hexadécimales.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Utilisez cet argument pour spécifier que les messages se terminent immédiatement après le corps du message. La valeur par défaut consiste à terminer le corps du message par un CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Utilisez cet argument pour que le compilateur génère un fichier d’en-tête OLE2 à l’aide de définitions **HRESULT** au lieu de codes d’État. L’utilisation de codes d’État est la valeur par défaut.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Utilisez cet argument pour spécifier que le fichier d’entrée de *nom* de fichier contient du contenu UTF-16LE. La valeur par défaut est le contenu ANSI. Si le fichier d’entrée contient une nomenclature, cet argument est ignoré.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Utilisez cet argument pour spécifier que les messages dans le fichier output. bin doivent être au format Unicode. Il s’agit de la valeur par défaut.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Utilisez cet argument pour générer une sortie détaillée.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *chemin*
</dt> <dd>

Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le fichier include. dbg C. Le fichier. dbg mappe les ID de message à leurs noms symboliques.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les arguments **-A** et **-MOF** sont déconseillés et seront supprimés à l’avenir.

Le compilateur accepte comme entrée un fichier manifeste (. Man) ou un fichier texte de message (. MC) et génère les fichiers suivants :

-   *nom de fichier*. h

    Fichier d’en-tête C/C++ qui contient les descripteurs d’événement, le GUID du fournisseur et les noms de symboles que vous référencez dans votre application.

-   *nom du fichier* TEMP. bin

    Fichier de ressources binaire qui contient le fournisseur et les métadonnées d’événement. Il s’agit de la ressource de modèle, qui est indiquée par le suffixe temporaire du nom de base du fichier.

-   Msg00001. bin

    Un fichier de ressources binaire pour chaque langue que vous spécifiez (par exemple, si votre manifeste contient des chaînes de message en-US et fr-FR, le compilateur génère Msg00001. bin et Msg00002. bin).

-   *nom de fichier*. RC

    Script du compilateur de ressources qui contient les instructions pour inclure chaque fichier. bin en tant que ressource.

Pour les arguments qui acceptent un chemin d’accès, le chemin d’accès peut être un chemin d’accès absolu, relatif ou UNC et il peut contenir des variables d’environnement.

**Avant la version 1.12.7051 de MC :** Le compilateur n’autorise pas les chemins d’accès relatifs ou les variables d’environnement.

le SDK Windows comprend le compilateur (mc.exe) dans le \\ dossier Bin.

## <a name="examples"></a>Exemples

L’exemple suivant compile un manifeste à l’aide des valeurs par défaut du compilateur.

``` syntax
mc spooler.man
```

L’exemple suivant compile le manifeste et place l’en-tête et les fichiers de ressources dans les dossiers spécifiés.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------------|
| Client minimal pris en charge | Windows 2000 Professionnel - \[Applications de bureau uniquement\] |
| Serveur minimal pris en charge | Windows 2000 Server - \[Applications de bureau uniquement\]       |
