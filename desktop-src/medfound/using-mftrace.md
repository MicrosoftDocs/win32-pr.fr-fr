---
description: MFTrace est un outil permettant de générer des journaux de suivi pour les applications Microsoft Media Foundation.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Utilisation de MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530644"
---
# <a name="using-mftrace"></a>Utilisation de MFTrace

MFTrace est un outil permettant de générer des journaux de suivi pour les applications Microsoft Media Foundation.

MFTrace utilise la bibliothèque detoures pour se raccorder aux appels d’API Media Foundation et générer des journaux de suivi. MFTrace peut également enregistrer les traces à partir de n’importe quel composant qui utilise Suivi d’v nements pour Windows (ETW) ou le préprocesseur de trace logiciel (WPP) pour générer des traces. Les journaux de suivi peuvent être générés en démarrant un nouveau processus à partir de MFTrace ou en attachant MFTrace à un processus existant.

## <a name="usage"></a>Usage

**mftrace** \[ **-a** *Process* \] \[ **-c** *fichier ConfigurationFile* \] \[ **-DC** \] \[ **-es** \] \[ **-k** *mots* \] \[ **-clés-l** *niveau* \] \[ **-o** *outputfile* \] \[ **-v** \] \[ **-** ? \] \[ {*Commande* \| *ETL_FILE*}\]




| Arguments de ligne de commande | Description | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>ID de processus ou nom de processus</em><br /> | Attacher à un processus en cours d’exécution.<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Fichier de configuration</em><br /> | Lit les paramètres du fichier de configuration spécifié. Consultez le <a href="mftrace-configuration-file.md">fichier de configuration MFTrace</a>.<br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br /> | Désactive le suivi pour les processus enfants. Par défaut, le suivi est activé pour les processus enfants.<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | Activez les symboles publics.<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Mots clés</em><br /> | Liste de mots clés séparés par des virgules. Consultez <a href="mftrace-keywords.md">MFTrace Keywords</a>.<br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> De <em>niveau</em><br /> | Niveau de trace.<br /><ul><li>0 : Aucun</li><li>1 : critique</li><li>2 : erreur</li><li>3 : AVERTISSEMENT</li><li>4 : informatif</li><li>5 : commentaires</li><li>16 : débogage</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Fichier de sortie</em><br /> | Écrit la sortie de suivi dans le fichier spécifié. Par défaut, la sortie est envoyée à <strong>stdout</strong>.<br /> Si un fichier de sortie est spécifié, l’extension de nom de fichier doit être l’une des suivantes :<br /><ul><li>. ETL : fichier journal de suivi d’événements (ETL).</li><li>fichier. log ou .txt : Text.</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | Activer le mode détaillé.<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | Affichez des informations sur l’utilisation.<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>COMMANDE</em><br /> | Arguments de ligne de commande pour créer un nouveau processus.<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | Nom d’un fichier ETL existant. Si cet argument est fourni, le fichier ETL est converti en sortie de texte.<br /> | 




 

## <a name="environment-variables"></a>Variables d'environnement

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

pour suivre les composants qui utilisent le Windows le préprocesseur de trace logiciel (WPP), définissez cette variable d’environnement sur le chemin d’accès aux fichiers de format de message de trace (TMF) du composant.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Si la recherche de symboles est activée (**-es**), définissez cette variable d’environnement pour spécifier le chemin d’accès aux symboles.

</dd> </dl>

## <a name="examples"></a>Exemples

Créer un processus et suivre ce processus :

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Attacher MFTrace à un processus existant :

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Envoyer la sortie de trace vers un fichier texte :

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Événements ETW de suivi ou WPP :

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> Le premier exemple génère un fichier texte. Le deuxième exemple génère un fichier ETL.

 

Conversion d’un fichier ETL en fichier texte :

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Notes

Par défaut, MFTrace génère uniquement des traces de détournements. Pour générer des traces ETW ou WPP, vous devez fournir un fichier de configuration. Le fichier de configuration donne les noms des fournisseurs de suivi. Pour plus d’informations, consultez [fichier de configuration MFTrace](mftrace-configuration-file.md).

MFTrace peut envoyer la sortie vers les destinations suivantes :

-   **stdout** (valeur par défaut).
-   Fichier texte.
-   Fichier ETL binaire.

Si vous journalisez des traces ETW/WPP, un fichier ETL est l’option la plus efficace, car les données de trace sont enregistrées en tant qu’objets BLOB binaires. Une fois la session de trace terminée, vous pouvez utiliser MFTrace pour convertir le fichier ETL en fichier texte.

> [!Note]  
> Pour le suivi des détournements, la sortie de texte est tout aussi efficace qu’un fichier ETL. Par conséquent, si vous consignez uniquement les traces de détourages (sans suivis ETW/WPP), la sortie de texte est recommandée.

 

Pour le suivi des détours, vous devez joindre MFTrace à un processus en cours d’exécution (**-a**) ou utiliser MFTrace pour créer un nouveau processus. Pour les traces ETW/WPP, MFTrace écoute tous les fournisseurs d’événements qui sont listés dans le fichier de configuration.

Vous pouvez filtrer les résultats de la trace en spécifiant des mots clés de trace à l’aide de l’option de ligne de commande **-k** ou dans le fichier de configuration. L’utilisation la plus courante, cependant, consiste à enregistrer toutes les traces, puis à utiliser un script ou **grep** pour rechercher des modèles de chaîne particuliers.

## <a name="interpreting-the-trace-results"></a>Interprétation des résultats de la trace

Vous pouvez utiliser MFTrace pour répondre à des questions sur ce qui se passe dans votre application ou composant Media Foundation. Le tableau suivant répertorie certaines questions typiques. La deuxième colonne fournit la chaîne de recherche qui peut aider à répondre à la question.




| Question | Rechercher des chaînes | 
|----------|----------------|
| Une erreur s’est produite ? | "0xc00d" | 
| La topologie a-t-elle été résolue correctement ? | « CTopologyHelpers :: trace » | 
| La session multimédia a-t-elle commencé ? | "MESessionStarted" | 
| Quel fichier a été lu ? | "CMFSourceResolverDetours" | 
| Quels sont les types de médias pour les flux sources ? | « Nouveau flux », « MENewStream », « CMFMediaSourceDetours :: TracePD » | 
| Les flux sources génèrent-ils des exemples ? | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| La lecture a-t-elle atteint la fin des données ? | "MEEndOfStream", "MEEndOfPresentation" | 
| Le format a-t-il changé ? | « MEStreamFormatChanged » (sources multimédias), « nouveau format », « MESessionStreamSinkFormatChanged » (récepteurs multimédia) | 
| Quels objets ont été créés ? | « COle32ExportDetours :: CoCreateInstance » | 
| Le Media Foundation transformations (MFTs) dans le pipeline traite-t-il des données ? | « CMFTransformDetours ::P rocessOutput », « CMFTransformDetours ::P rocessInput » | 
| Quels sont les États définis sur le MFTs ? | « CMFTransformDetours ::P rocessMessage » | 
| Une requête MFT a-t-elle des données d’entrée ? | « MF_E_TRANSFORM_NEED_MORE_INPUT » (MFT synchrone), « METransformNeedInput » (MFT asynchrone). | 
| Une table MFT asynchrone génère-t-elle des données de sortie ? | « ProcessOutputs disponible » | 
| Des exemples de demandes de récepteur multimédia ont-ils été exécutés ? | "MEStreamSinkRequestSample" | 
| Un récepteur multimédia a-t-il reçu des exemples ? | « CMFStreamSinkDetours ::P rocessSample » | 
| DirectShow : quels exemples ont été traités ? | "sample", "CMemInputPinDetours" | 
| DirectShow : quel graphique de filtre a été utilisé ? | « CGraphHelpers :: trace » | 
| Y a-t-il plusieurs processus ? | CreateProcess<blockquote>[!Note]<br />Recherchez également l’identificateur de processus, qui apparaît au début de chaque ligne de suivi.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




