---
title: Annotations d’en-tête
description: Les annotations d’en-tête décrivent comment une fonction utilise ses paramètres et sa valeur de retour.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API, annotations de fichier d’en-tête
- annotations du fichier d’en-tête
- Specstrings. h
- langage d’annotation standard (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ad560d00c45714d0feaa9ab2fa58ff4c985730fd563d4943ff028f561f2793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643629"
---
# <a name="header-annotations"></a>Annotations d’en-tête

\[cette rubrique décrit les annotations prises en charge dans les en-têtes de Windows via Windows 7. si vous développez pour Windows 8, vous devez utiliser les annotations décrites dans les [annotations SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

Les annotations d’en-tête décrivent comment une fonction utilise ses paramètres et sa valeur de retour. ces annotations ont été ajoutées à de nombreux fichiers d’en-tête de Windows pour vous aider à vous assurer que vous appelez correctement l’API Windows. si vous activez l’analyse du code, qui est disponible à partir de la Visual Studio 2005, le compilateur produira des avertissements de niveau 6000 si vous n’appelez pas ces fonctions selon l’utilisation décrite par les annotations. Vous pouvez également ajouter ces annotations dans votre propre code pour vous assurer qu’elles sont appelées correctement. pour activer l’analyse du code dans Visual Studio, consultez la documentation de votre version de Visual Studio.

Ces annotations sont définies dans Specstrings. h. Ils reposent sur les primitives qui font partie du langage de l’annotation standard (SAL) et implémentent à l’aide de `_declspec("SAL_*")` .

Il existe deux classes d’annotations : les annotations de mémoire tampon et les annotations avancées.

## <a name="buffer-annotations"></a>Annotations de mémoire tampon

Les annotations de mémoire tampon décrivent comment les fonctions utilisent leurs pointeurs et peuvent être utilisées pour détecter les dépassements de mémoire tampon. Chaque paramètre peut utiliser zéro ou une annotation de mémoire tampon. Une annotation de mémoire tampon est construite avec un trait de soulignement de début et les composants décrits dans les sections suivantes.



| buffer_size                                                                                  | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*taille*)<br/>                        | Spécifie la taille totale de la mémoire tampon. Utilisez avec \_ bcount et \_ ecount ; n’utilisez pas with \_ part. Cette valeur est l’espace accessible ; Il peut être inférieur à l’espace alloué.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*taille*,*longueur*)<br/> | Spécifie la taille totale et la longueur initialisée de la mémoire tampon. Utilisez avec la partie \_ bcount \_ et \_ ecount \_ . La taille totale peut être inférieure à l’espace alloué.<br/>              |



 



| Unités de taille de la mémoire tampon                                                       | Description                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | La taille de la mémoire tampon est en octets.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | La taille de la mémoire tampon est dans les éléments.<br/> |



 



| Sens                                                            | Description                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_dans<br/>          | La fonction lit à partir de la mémoire tampon. L’appelant fournit la mémoire tampon et l’initialise.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_INOUT<br/> | La fonction lit et écrit dans la mémoire tampon. L’appelant fournit la mémoire tampon et l’initialise. S’il est utilisé avec \_ Deref, la mémoire tampon peut être réallouée par la fonction.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_à<br/>       | La fonction écrit dans la mémoire tampon. S’il est utilisé sur la valeur de retour ou avec \_ Deref, la fonction fournit la mémoire tampon et l’initialise. Dans le cas contraire, l’appelant fournit la mémoire tampon et la fonction l’initialise.<br/> |



 



| Adressage indirect                                                                       | Description                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Déréférencez le paramètre pour obtenir le pointeur de la mémoire tampon. Ce paramètre ne peut pas être **null**.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_option \_ Deref<br/> | Déréférencez le paramètre pour obtenir le pointeur de la mémoire tampon. Ce paramètre peut être **NULL**.<br/>     |



 



| Initialisation                                                    | Description                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_sauvegarde<br/> | La fonction initialise la mémoire tampon entière. À utiliser uniquement avec les mémoires tampons de sortie.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_étape<br/> | La fonction Initialise une partie de la mémoire tampon et indique explicitement le volume. À utiliser uniquement avec les mémoires tampons de sortie.<br/> |



 



| Mémoire tampon obligatoire ou facultative                                    | Description                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_possibilité<br/> | Ce paramètre peut être **NULL**.<br/> |



 

L’exemple suivant montre les annotations pour la fonction **GetModuleFileName** . Le paramètre *HMODULE* est un paramètre d’entrée facultatif. Le paramètre *lpFilename* est un paramètre de sortie ; sa taille en caractères est spécifiée par le paramètre *nSize* et sa longueur comprend le caractère de fin **null**. Le paramètre *nSize* est un paramètre d’entrée.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Voici les annotations définies dans Specstrings. h. Utilisez les informations des tableaux ci-dessus pour interpréter leur signification.

__bcount (*taille*)  
__bcount_opt (*taille*)  
__deref_bcount (*taille*)  
__deref_bcount_opt (*taille*)  
__deref_ecount (*taille*)  
__deref_ecount_opt (*taille*)  
__deref_in  
__deref_in_bcount (*taille*)  
__deref_in_bcount_opt (*taille*)  
__deref_in_ecount (*taille*)  
__deref_in_ecount_opt (*taille*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*taille*)  
__deref_inout_bcount_full (*taille*)  
__deref_inout_bcount_full_opt (*taille*)  
__deref_inout_bcount_opt (*taille*)  
__deref_inout_bcount_part (*taille*,*longueur*)  
__deref_inout_bcount_part_opt (*taille*,*longueur*)  
__deref_inout_ecount (*taille*)  
__deref_inout_ecount_full (*taille*)  
__deref_inout_ecount_full_opt (*taille*)  
__deref_inout_ecount_opt (*taille*)  
__deref_inout_ecount_part (*taille*,*longueur*)  
__deref_inout_ecount_part_opt (*taille*,*longueur*)  
__deref_inout_opt  
__deref_opt_bcount (*taille*)  
__deref_opt_bcount_opt (*taille*)  
__deref_opt_ecount (*taille*)  
__deref_opt_ecount_opt (*taille*)  
__deref_opt_in  
__deref_opt_in_bcount (*taille*)  
__deref_opt_in_bcount_opt (*taille*)  
__deref_opt_in_ecount (*taille*)  
__deref_opt_in_ecount_opt (*taille*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*taille*)  
__deref_opt_inout_bcount_full (*taille*)  
__deref_opt_inout_bcount_full_opt (*taille*)  
__deref_opt_inout_bcount_opt (*taille*)  
__deref_opt_inout_bcount_part (*taille*,*longueur*)  
__deref_opt_inout_bcount_part_opt (*taille*,*longueur*)  
__deref_opt_inout_ecount (*taille*)  
__deref_opt_inout_ecount_full (*taille*)  
__deref_opt_inout_ecount_full_opt (*taille*)  
__deref_opt_inout_ecount_opt (*taille*)  
__deref_opt_inout_ecount_part (*taille*,*longueur*)  
__deref_opt_inout_ecount_part_opt (*taille*,*longueur*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*taille*)  
__deref_opt_out_bcount_full (*taille*)  
__deref_opt_out_bcount_full_opt (*taille*)  
__deref_opt_out_bcount_opt (*taille*)  
__deref_opt_out_bcount_part (*taille*,*longueur*)  
__deref_opt_out_bcount_part_opt (*taille*,*longueur*)  
__deref_opt_out_ecount (*taille*)  
__deref_opt_out_ecount_full (*taille*)  
__deref_opt_out_ecount_full_opt (*taille*)  
__deref_opt_out_ecount_opt (*taille*)  
__deref_opt_out_ecount_part (*taille*,*longueur*)  
__deref_opt_out_ecount_part_opt (*taille*,*longueur*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*taille*)  
__deref_out_bcount_full (*taille*)  
__deref_out_bcount_full_opt (*taille*)  
__deref_out_bcount_opt (*taille*)  
__deref_out_bcount_part (*taille*,*longueur*)  
__deref_out_bcount_part_opt (*taille*,*longueur*)  
__deref_out_ecount (*taille*)  
__deref_out_ecount_full (*taille*)  
__deref_out_ecount_full_opt (*taille*)  
__deref_out_ecount_opt (*taille*)  
__deref_out_ecount_part (*taille*,*longueur*)  
__deref_out_ecount_part_opt (*taille*,*longueur*)  
__deref_out_opt  
__ecount (*taille*)  
__ecount_opt (*taille*)  
__in  
__in_bcount (*taille*)  
__in_bcount_opt (*taille*)  
__in_ecount (*taille*)  
__in_ecount_opt (*taille*)  
__in_opt  
__inout  
__inout_bcount (*taille*)  
__inout_bcount_full (*taille*)  
__inout_bcount_full_opt (*taille*)  
__inout_bcount_opt (*taille*)  
__inout_bcount_part (*taille*,*longueur*)  
__inout_bcount_part_opt (*taille*,*longueur*)  
__inout_ecount (*taille*)  
__inout_ecount_full (*taille*)  
__inout_ecount_full_opt (*taille*)  
__inout_ecount_opt (*taille*)  
__inout_ecount_part (*taille*,*longueur*)  
__inout_ecount_part_opt (*taille*,*longueur*)  
__inout_opt  
__out  
__out_bcount (*taille*)  
__out_bcount_full (*taille*)  
__out_bcount_full_opt (*taille*)  
__out_bcount_opt (*taille*)  
__out_bcount_part (*taille*,*longueur*)  
__out_bcount_part_opt (*taille*,*longueur*)  
__out_ecount (*taille*)  
__out_ecount_full (*taille*)  
__out_ecount_full_opt (*taille*)  
__out_ecount_opt (*taille*)  
__out_ecount_part (*taille*,*longueur*)  
__out_ecount_part_opt (*taille*,*longueur*)  
__out_opt  

## <a name="advanced-annotations"></a>Annotations avancées

Les annotations avancées fournissent des informations supplémentaires sur le paramètre ou la valeur de retour. Chaque paramètre ou valeur de retour peut utiliser zéro ou une annotation avancée.



| Annotation                                                                                                                                               | Description                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*ressource*)<br/> | Les fonctions se bloquent sur la ressource spécifiée.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_rappel<br/>                                                                        | La fonction peut être utilisée comme pointeur de fonction.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | Les appelants doivent vérifier la valeur de retour.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_chaîne de format \_<br/>                                                        | Le paramètre est une chaîne qui contient des marqueurs% de style printf.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_dans \_ awcount (*expr*,*taille*)<br/>                            | Si l’expression a la valeur true à la sortie, la taille de la mémoire tampon d’entrée est spécifiée en octets. Si l’expression a la valeur false, la taille est spécifiée dans les éléments.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | La mémoire tampon peut être accessible jusqu’à la première séquence de deux caractères ou pointeurs **null** , y compris.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | La mémoire tampon peut être accessible jusqu’à et y compris le premier caractère ou pointeur **null** .<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*taille*)<br/>                         | Si l’expression a la valeur true à la sortie, la taille de la mémoire tampon de sortie est spécifiée en octets. Si l’expression a la valeur false, la taille est spécifiée dans les éléments. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_remplacer<br/>                                                                        | Spécifie le comportement de substitution de style C# pour les méthodes virtuelles.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_réservé<br/>                                                                        | Le paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro ou **null**.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_opération réussie (*expr*)<br/>                                                       | Si l’expression a la valeur true à la sortie, l’appelant peut s’appuyer sur toutes les garanties spécifiées par d’autres annotations. Si l’expression a la valeur false, l’appelant ne peut pas compter sur les garanties. Cette annotation est automatiquement ajoutée aux fonctions qui retournent une valeur **HRESULT** .<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Traite le paramètre en tant que type spécifié plutôt qu’en tant que type déclaré.<br/>                                                                                                                                                                                             |



 

Les exemples suivants illustrent la mémoire tampon et les annotations avancées pour les fonctions [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)et [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annotations SAL](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Procédure pas à pas : analyse du code C/C++ pour rechercher les erreurs](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

