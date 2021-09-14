---
description: Exemple de filtre de l’analyseur PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Exemple de filtre de l’analyseur PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094649"
---
# <a name="psi-parser-filter-sample"></a>Exemple de filtre de l’analyseur PSI

## <a name="description"></a>Description

Le filtre de l’analyseur PSI reçoit des informations spécifiques au programme (PSI) à partir d’un flux de transport MPEG-2 et extrait les informations de programme de la table d’association de programmes (PAT) et des tables de cartes de programme (VPM). Ces informations permettent à une application de configurer le démultiplexeur MPEG-2. Le filtre prend en charge une interface personnalisée, [**IMpeg2PsiParser**](impeg2psiparser.md), pour récupérer les informations psi.

Ce filtre est conçu pour les appareils MPEG-2, tels que les caméscopes IEEE 1394 MPEG-2 et les appareils D-VHS. Pour plus d’informations, consultez [pilote MSTape](mstape-driver.md) . Les sources de diffusion de télévision numérique doivent utiliser un filtre TIF pour obtenir des informations sur le programme.

## <a name="usage"></a>Usage

Vous pouvez tester le filtre de l’analyseur PSI dans GraphEdit comme suit :

1.  Lancez GraphEdit.
2.  Insérez une source de transport MPEG-2. Les caméscopes MPEG-2 et les appareils D-VHS apparaissent en tant que « périphérique de sous-unité de bande Microsoft AV/C » dans la catégorie sources de capture vidéo.
3.  Connecter le filtre source au filtre de démultiplexage MPEG-2.
4.  Utilisez la page de propriétés de demux pour créer une broche de sortie avec un type de média « PSI MPEG-2 PSI ». Ce code PIN propose les sections PAT et VPM.
5.  Utilisez la page de propriétés demux pour mapper PID 0x00 à la broche de sortie. Définissez le type de contenu sur « sections PSI PSI ».
6.  Connecter la broche de sortie demux à l’analyseur PSI, comme indiqué dans le diagramme suivant.

    ![graphique de filtre de l’analyseur psi](images/psi-parser.png)

7.  Exécutez le graphique afin d’alimenter les données PSI vers le filtre de l’analyseur PSI. Au fur et à mesure que le filtre décode les sections PAT, il mappe automatiquement les pid PMT à la même broche de sortie sur le demux, afin qu’il reçoive les sections VPM.
8.  Utilisez la page de propriétés de l’analyseur PSI pour sélectionner un numéro de programme. La liste de flux élémentaires de la page de propriétés indique le PID et le type de flux associés à chaque flux élémentaire dans le programme sélectionné. La page de propriétés est conçue pour reconnaître les types de flux définis dans la norme ISO/IEC 13818-1.
9.  Entrez le numéro PID Audio dans la zone d’édition des **PID Audio** et le numéro PID de la vidéo dans la zone d’édition de la **vidéo PID** .
10. Cliquez sur le bouton **afficher le programme** . L’analyseur PSI configure les broches de sortie sur le demux pour qu’elles correspondent aux informations de flux de programme et restitue les codes confidentiels.

> [!Note]  
> La page de propriétés de l’analyseur PSI est fournie pour faciliter le test et pour fournir un exemple de code qui configure le démultiplexeur MPEG-2. Elle n’est pas recommandée pour les applications. Les applications doivent configurer demux par programme.

 

Pour utiliser le filtre de l’analyseur PSI dans une application, commencez par créer le graphique de filtre de la source MPEG-2 sur le demux MPEG-2. Le code pour cette étape n’est pas indiqué ici, car la configuration exacte du graphique dépend de la source.

Ensuite, créez une broche de sortie sur le demux pour les données PSI. Mappez le PID 0x00, qui est réservé aux sections PAT, à ce code PIN, comme indiqué dans le code suivant :


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



Pour plus d’informations, consultez [utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md).

Ajoutez le filtre de l’analyseur PSI au graphique et connectez-le à la broche de sortie sur le demux. Interrogez l’analyseur PSI pour l’interface [**IMpeg2PsiParser**](impeg2psiparser.md) . Exécutez maintenant le graphique et attendez les \_ événements de changement de programme EC \_ qui signalent une nouvelle section Pat ou VPM. Cet événement est un événement personnalisé défini par le filtre de l’analyseur PSI. Lorsque vous recevez un \_ événement de changement de programme EC \_ , vous pouvez obtenir les informations PSI disponibles en appelant les méthodes **IMpeg2PsiParser** . Cette section décrit les méthodes dont vous aurez besoin le plus souvent.

Pour connaître le nombre de programmes, utilisez la méthode [**IMpeg2PsiParser :: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Pour obtenir le numéro de programme d’un programme spécifique, utilisez la méthode [**IMpeg2PsiParser :: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



Le numéro de programme est utilisé pour obtenir les entrées VPM pour des programmes individuels. Pour obtenir le nombre de flux élémentaires dans un programme, utilisez la méthode [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Pour chaque flux élémentaire, la méthode [**IMpeg2PsiParser :: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) retourne le PID, et la méthode [**IMpeg2PsiParser :: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) retourne le type de flux :


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



Le PID et le type de flux vous permettent de configurer de nouvelles broches de sortie sur le démultiplexeur MPEG-2. Cela peut nécessiter une connaissance de la source d’origine. Par exemple, la norme ISO/IEC 13818-1 définit les types de flux 0x80 à 0xFF comme « Private User », mais d’autres normes basées sur MPEG-2 peuvent attribuer d’autres significations à ces types.

Le démultiplexeur MPEG-2 peut créer des codes confidentiels et de nouveaux mappages PID lorsque le graphique est en cours d’exécution, mais vous devez arrêter le graphique pour connecter les broches.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ \\ PSIParser filtres de DirectShow \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> </dl>

 

 
